---
title: Generar informes de Analytics
description: Aprenda a utilizar la habilidad de Surface Analytics en el chat de Coworker para generar informes de actividad, correo electrónico, posibles clientes, segmentos y recorridos a partir de mensajes en lenguaje natural.
autotag-review: '2026-09-21T14:58:26.479Z'
TQID: 'https://experienceleague.adobe.com/BSDEihjdpz-YZjMWrYTmIuyjqtcjRHRrJdz4xPFZbHU'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 1650dadf-b034-5ac9-a309-77ad1e2f5035
    internal-label: Chat Interface
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
subfeature_v2:
  - id: b9e5c7f3-be30-563c-9e41-cc8ea76e2fee
    internal-label: Skills
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
source-git-commit: 1dcc3bcdc59114c7fc1e16178db8921ae173b955
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%
---
# Generar informes de análisis

La habilidad [_Surface Analytics_](./skills.md#analytics-reporting) en [!DNL Adobe Marketo Optimizer] responde a preguntas sobre tus datos en lenguaje natural. Utilícelo en la [interfaz de chat de compañeros](./chat-interface.md) para explorar las tendencias de actividad, el rendimiento del correo electrónico, los datos de clientes potenciales y cuentas, la pertenencia a segmentos y listas y las métricas de recorridos. Los resultados se devuelven como gráficos y tablas, por lo que no es necesario crear una consulta o panel manualmente.

* **Habilidad** - `surface-analytics`
* **Invocación**: haga una pregunta en lenguaje natural o use un comando de barra diagonal para ejecutar la habilidad de Surface Analytics. Por ejemplo: _&quot;Mostrarme los recuentos diarios de actividad de los últimos 30 días.&quot;_
* **Lee de** - [!DNL Marketo Optimizer] datos de análisis; lee [!DNL Marketo Engage] datos de análisis para preguntas que abarcan ambos productos

>[!NOTE]
>
>Los datos del informe se actualizan cada dos horas. Los resultados pueden no reflejar la actividad de las últimas dos horas.

## Ver tendencias de la actividad {#activity-trends}

Pregunte por los recuentos de actividades diarias o semanales y desglose los resultados por tipo de actividad o área de producto.

* _&quot;Mostrarme los recuentos diarios de actividad de los últimos 30 días.&quot;_
* _&quot;¿Cuáles son los tipos de actividades principales de esta semana?&quot;_
* _&quot;Desglosar la actividad del mes pasado por área de aplicación.&quot;_

## Comprobar rendimiento de correo electrónico {#email-performance}

Pregunte por el volumen de envío, las tasas de apertura y clics, los rechazos y las cancelaciones de suscripción de sus programas de correo electrónico.

* _&quot;¿Cuál es la tasa de apertura de correo electrónico por recorrido?&quot;_
* _&quot;Mostrarme las tasas de clics de los últimos 90 días.&quot;_
* _&quot;¿Cuántas cancelaciones de suscripción obtuvimos la semana pasada?&quot;_

## Analizar datos de clientes potenciales y cuentas {#lead-account-data}

Pregunte por la distribución de puntuación de posibles clientes, desgloses personales y resúmenes geográficos o firmográficos.

* _&quot;Mostrarme la distribución de puntuación entre posibles clientes.&quot;_
* _&quot;¿Cuántas personas hay en cada cuenta?&quot;_
* _&quot;Desglosar posibles clientes por persona.&quot;_

## Revisar abono de segmentos y listas {#segment-list-membership}

Pregunte quién pertenece a una lista o segmento específico.

* _&quot;¿Cuántas personas hay en la lista de nutrición del primer trimestre?&quot;_
* _&quot;¿Qué segmento tiene la mayor cantidad de miembros?&quot;_

## Explorar métricas de recorrido {#journey-metrics}

Pregunte por el abono a recorridos, las tasas de finalización, el recorrido de nodos y el análisis de funnel.

* _&quot;¿Cuál es la tasa de finalización del recorrido de seguimiento de demostración?&quot;_
* _&quot;¿Cuántas personas hay en cada nodo de LeadNutureJourney?&quot;_

## Hacer preguntas entre productos {#cross-product}

Surface Analytics puede responder preguntas que abarcan datos de [!DNL Marketo Engage] y [!DNL Marketo Optimizer] en una sola solicitud.

* _&quot;¿Cuál es mi correo electrónico de mayor rendimiento en LumaSecure y en LumaStorage?&quot;_

## Limitaciones {#limitations}

| Limitación | Detalles |
|---|---|
| Edición o creación de registros | No compatible. Surface Analytics solo lee e informa sobre datos existentes. |
| Nombres legibles por humanos en los resultados | No siempre disponible. Algunos informes muestran un ID interno, como un ID de recorrido o de correo electrónico, en lugar de un nombre. |
| Duplicar tarjetas de informes | Una sola pregunta puede devolver ocasionalmente más de una tarjeta de informe para el mismo resultado. |
