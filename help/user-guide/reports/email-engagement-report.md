---
title: Informe de participación por correo electrónico
description: Obtenga información acerca del informe Participación por correo electrónico en Adobe Marketo Optimizer, que muestra las métricas de participación y capacidad de entrega de correo electrónico por correo electrónico y recorrido.
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
source-git-commit: 8c47a9c69c32ba0a37ba2efadb6ad4c1b796c21d
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%
---

# Informe Participación por correo electrónico

<!-- SPHR-39569: content drafted, but hide: true and hide-from-toc stay until eng confirms this shipped to production. Filter by Program, Filter by Audience, and the program data point from SPHR-32511 are not documented here pending delivery-state confirmation. -->

Use el informe [!UICONTROL Participación por correo electrónico] para revisar la capacidad de entrega de correo electrónico y el rendimiento de la participación en toda la instancia, desglosados por correo electrónico y recorrido.

_Para ver el informe :_

1. En el panel de navegación izquierdo, seleccione **[!UICONTROL Informes]**.
1. Haga clic en el icono _Lista_ ( ![Icono de lista](../assets/do-not-localize/icon-table-of-contents.svg) ) y seleccione **[!UICONTROL Participación por correo electrónico]** en el panel _[!UICONTROL Tabla de contenido]_.

![Informe de participación por correo electrónico con filtros de nombre de Recorrido y de persona, un intervalo de fechas de los últimos 30 días y una tabla de métricas de actividad de correo electrónico.](./assets/reports-email-engagement.png){width="700" zoomable="yes"}

Puede [cambiar el intervalo de fechas](./reports-overview.md#change-the-date-range) con el mismo selector de intervalo de fechas disponible en otras secciones del informe.

Seleccione **[!UICONTROL Compartir]** en la parte superior del informe para descargar o programar una exportación de todos los datos del informe. Consulte [_Exportar un informe_](./reports-overview.md#export-a-report) en la descripción general de informes.

## Tabla del informe {#report-table}

El informe [!UICONTROL Participación por correo electrónico] muestra una fila por cada correo electrónico, con las siguientes dimensiones de fila.

* **[!UICONTROL Nombre de correo electrónico]** - El nombre del correo electrónico.
* **[!UICONTROL Nombre de Recorrido]** - El nombre del recorrido que envió el correo electrónico.

Las columnas de métricas se agrupan en **[!UICONTROL Actividades de correo electrónico]**.

| Columna | Descripción |
| --- | --- |
| [!UICONTROL Enviado] | Número de correos electrónicos enviados. |
| [!UICONTROL Entregado] | Número de correos electrónicos enviados. |
| [!UICONTROL % Entregado] | Porcentaje de correos electrónicos enviados que se entregaron. |
| [!UICONTROL Rechazado fuerte] | Número de correos electrónicos que no se entregaron de forma permanente. |
| [!UICONTROL Rechazado suave] | Número de correos electrónicos que no se entregaron temporalmente. |
| [!UICONTROL Abierto] | Número de veces que los destinatarios abrieron el correo electrónico. |
| [!UICONTROL % abierto] | Porcentaje de correos electrónicos enviados que se han abierto. |
| [!UICONTROL Se hizo clic] | Número de veces que los destinatarios hicieron clic en un vínculo del correo electrónico. |
| [!UICONTROL % hizo clic] | Porcentaje de correos electrónicos enviados que recibieron un clic. |
| [!UICONTROL Proporción de clics para abrir] | Porcentaje de correos electrónicos abiertos que recibieron un clic. |
| [!UICONTROL Canceló la suscripción] | Número de destinatarios que cancelaron la suscripción al correo electrónico. |
| [!UICONTROL % canceló la suscripción] | Porcentaje de correos electrónicos enviados que tuvieron como resultado una cancelación de suscripción. |

<!--

## Filters {#filters}

Use filters to narrow the report to a specific journey, persona, or date range. Select **[!UICONTROL Reset all]** to clear every filter and return to the default view.

* **[!UICONTROL Journey Name (Event)]** - Filter by the journey that sent the email. Default is [!UICONTROL No filter].
* **[!UICONTROL Persona (Event)]** - Filter by the persona associated with the email. Default is [!UICONTROL No filter].
* **[!UICONTROL Date range]** - Filter by a specific date span, shown as explicit start and end dates. Default is [!UICONTROL Last 30 days].
-->