---
title: Arquitectura de alto nivel
description: Obtenga información acerca de la arquitectura de datos que conecta Marketo Optimizer y Marketo Engage, incluida la sincronización bidireccional, la latencia de la entidad y el aislamiento de datos del inquilino.
role: User, Admin
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 2%

---


# Arquitectura de alto nivel

[!DNL Adobe Marketo Optimizer] se integra con [!DNL Adobe Marketo Engage] para ofrecer una vista de 360 grados de los posibles clientes B2B. Una sincronización bidireccional y de confianza mantiene alineados a Marketo Engage y Marketo Optimizer, lo que proporciona a ambas plataformas una sola vista compartida de Personas, Compañías, Objetos personalizados y Actividades. El flujo de datos de alto rendimiento y casi en tiempo real garantiza que los registros estén actualizados y sean procesables, de modo que las campañas y los recorridos puedan responder a los posibles clientes en el momento en que interactúen.

## Base de datos

[!DNL Marketo Optimizer] y [!DNL Marketo Engage] comparten una base de datos común que mantiene ambas plataformas sincronizadas mientras se alimenta el análisis descendente.

![Diagrama de arquitectura de Marketo Optimizer y Marketo Engage que muestra cómo se conectan los servicios, los tiempos de ejecución y los almacenes de datos de los dos productos entre Microsoft Azure y AWS](./assets/marketo-optimizer-architecture.svg)

En un nivel superior:

* **Marketo Engage Core** es la fuente definitiva de datos de objetos personalizados y posibles clientes, lo que garantiza la integridad de los datos en el punto de captura.
* Un **nivel de Data Broker** coordina cómo se mueven los datos entre Marketo Engage y Marketo Optimizer, agregando datos compartidos y replicados en un entorno operativo y listo para usar. Todo este intercambio se ejecuta dentro de una sola instancia compartida de AWS Aurora, formando la base de bucle cerrado para la orquestación B2B de alta escala.
* **Las actividades** siguen una ruta definida: primero se escriben en la base de datos de Marketo Engage y se indexan en Apache SOLR para una búsqueda rápida dentro del producto; después, se publican en la canalización de actividades para que Marketo Optimizer tenga conocimiento instantáneo. El tiempo de ejecución de Recorrido procesa esa actividad y la escribe en Snowflake, transformando los datos operativos en un estado listo para análisis. A partir de ahí, la actividad se replica en los conjuntos de datos de AEP y CJA para potenciar los informes.
* Los distintos tipos de entidades se sincronizan a diferentes velocidades y direcciones para equilibrar la frescura con la integridad del sistema:

| Entidad de Marketo Engage | Dirección de sincronización | Latencia |
| --- | --- | --- |
| Posible cliente | Bidireccional | &lt; 1 s |
| Compañía | Bidireccional | &lt; 1 s |
| Objeto personalizado | Unidireccional | &lt; 5 s |
| Actividad | Unidireccional | &lt; 5 s |
| Suscripción al programa | No sincronizado | — |
| Recursos | No sincronizado | — |

Los posibles clientes y las empresas se actualizan instantáneamente en ambas direcciones sin crear copias de datos duplicadas. Los objetos personalizados se replican en segundos, por lo que las actualizaciones de esquema en Marketo Engage se pueden procesar inmediatamente en un recorrido activo. La pertenencia al programa y Assets se excluyen intencionadamente de la sincronización para preservar la velocidad y la integridad del sistema.

Este diseño de latencia casi nulo significa que los paneles de análisis y los sistemas descendentes se alimentan en tiempo casi real, lo que permite la optimización de campañas en directo y el seguimiento rápido de posibles clientes de alta prioridad.

### Aislamiento y tenencia de datos

* Los datos del cliente se comparten entre Marketo Engage, Marketo Optimizer y Experience Platform como parte de la sincronización de datos del producto y la arquitectura de análisis.
* Los datos están aislados lógicamente por inquilino y protegidos por controles de seguridad de Adobe.
* Los datos se transfieren a través de canales seguros y cifrados y se almacenan en servicios administrados por Adobe mediante el cifrado y los controles de acceso estándar del sector.
* Según el tipo de datos, la información se puede sincronizar entre Marketo Engage y Marketo Optimizer o replicarse en Experience Platform para admitir las funciones de informes y análisis, manteniendo al mismo tiempo la seguridad y el aislamiento del inquilino.
