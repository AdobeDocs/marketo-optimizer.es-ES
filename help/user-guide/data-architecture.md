---
title: Arquitectura de alto nivel
description: Obtenga información acerca de la arquitectura de datos que conecta Marketo Optimizer y Marketo Engage, incluida la sincronización bidireccional, la latencia de la entidad y el aislamiento de datos del inquilino.
role: User, Admin
TQID: 'https://experienceleague.adobe.com/oelEtys81g6TzM8bi-qy1nuWw6scOBry7tbZkMkZ6u0'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 3c1de303-7a7c-59a6-abca-8c534730e19cid: 64b90904-e4f0-5c1b-a871-8c6a40b204a1id: d4203578-d294-5145-b397-f26f4488a904
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d00e9f03-e50b-4162-b143-0c0817c937c2id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 451
ht-degree: 1%

---


# Arquitectura de alto nivel

[!DNL Adobe Marketo Optimizer] se integra con [!DNL Adobe Marketo Engage] para ofrecer una vista de 360 grados de los posibles clientes B2B. Una sincronización bidireccional y de confianza mantiene alineados a [!DNL Marketo Engage] y a [!DNL Marketo Optimizer], lo que proporciona a ambas plataformas una única vista compartida de Personas, Compañías, Objetos personalizados y Actividades. El flujo de datos de alto rendimiento y casi en tiempo real garantiza que los registros estén actualizados y sean procesables, de modo que las campañas y los recorridos puedan responder a los posibles clientes en el momento en que interactúen.

## Base de datos

[!DNL Marketo Optimizer] y [!DNL Marketo Engage] comparten una base de datos común que los mantiene sincronizados mientras se alimentan los análisis descendentes.

![Diagrama de arquitectura de Marketo Optimizer y Marketo Engage que muestra cómo se conectan los servicios, los tiempos de ejecución y los almacenes de datos de los dos productos entre Microsoft Azure y AWS](./assets/marketo-optimizer-architecture.svg)

En un nivel superior:

* **[!DNL Marketo Engage]Core** es el origen definitivo de los datos de los objetos personalizados y de posibles clientes, lo que garantiza la integridad de los datos en el punto de captura.
* Una capa de **agente de datos** coordina cómo se mueven los datos entre [!DNL Marketo Engage] y [!DNL Marketo Optimizer], agregando datos compartidos y replicados en un entorno operativo y listo para usar. Todo este intercambio se ejecuta dentro de una sola instancia compartida de AWS Aurora, formando la base de bucle cerrado para la orquestación B2B de alta escala.
* **Las actividades** siguen una ruta de acceso definida: primero se escriben en la base de datos [!DNL Marketo Engage] y se indexan en Apache SOLR para realizar búsquedas rápidas dentro del producto; después, se publican en la canalización de actividades para que [!DNL Marketo Optimizer] tenga conocimiento instantáneo. El tiempo de ejecución de recorrido procesa esa actividad y la escribe en Snowflake, transformando los datos operativos en un estado listo para análisis. A partir de ahí, la actividad se replica en [!DNL Adobe Experience Platform] conjuntos de datos y en [!DNL Adobe Customer Journey Analytics] para activar los informes.
* Los distintos tipos de entidades se sincronizan a diferentes velocidades y direcciones para equilibrar la frescura con la integridad del sistema:

| [!DNL Marketo Engage] entidad | Dirección de sincronización | Latencia |
| --- | --- | --- |
| Posible cliente | Bidireccional | &lt; 1 s |
| Compañía | Bidireccional | &lt; 1 s |
| Objeto personalizado | Unidireccional | &lt; 5 s |
| Actividad | Unidireccional | &lt; 5 s |
| abono al programa | No sincronizado | — |
| Recursos | No sincronizado | — |

Los posibles clientes y las empresas se actualizan instantáneamente en ambas direcciones sin crear copias de datos duplicadas. Los objetos personalizados se replican en cuestión de segundos, por lo que las actualizaciones de esquema de [!DNL Marketo Engage] se pueden procesar inmediatamente en un recorrido activo. La pertenencia al programa y Assets se excluyen intencionadamente de la sincronización para preservar la velocidad y la integridad del sistema.

Este diseño de latencia casi nulo significa que los paneles de análisis y los sistemas descendentes se alimentan en tiempo casi real, lo que permite la optimización de campañas en directo y el seguimiento rápido de posibles clientes de alta prioridad.

### Aislamiento y tenencia de datos

* Los datos del cliente se comparten entre [!DNL Marketo Engage], [!DNL Marketo Optimizer] y [!DNL Experience Platform] como parte de la sincronización de datos del producto y la arquitectura de análisis.
* Los datos están aislados lógicamente por inquilino y protegidos por controles de seguridad de Adobe.
* Los datos se transfieren a través de canales seguros y cifrados y se almacenan en servicios administrados por Adobe mediante el cifrado y los controles de acceso estándar del sector.
* Según el tipo de datos, la información se puede sincronizar entre [!DNL Marketo Engage] y [!DNL Marketo Optimizer] o replicarse en [!DNL Experience Platform] para admitir las capacidades de informes y análisis, manteniendo al mismo tiempo la seguridad y el aislamiento del inquilino.
