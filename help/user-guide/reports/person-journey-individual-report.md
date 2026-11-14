---
title: Informe Detalles del Recorrido de personas
description: Obtenga información acerca del informe de detalles del Recorrido de persona en Adobe Marketo Optimizer, que muestra las métricas de finalización, participación y correo electrónico de los recorridos seleccionados.
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
source-git-commit: 84abcbf4ddf114898768766d6e91ec855e3f979f
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%
---

# Informe de detalles del Recorrido de personas

<!-- SPHR-39120: UX plans to move the Journey activity flow tile to the top of the report. Update the tile order in this page when that ships. -->

Haga clic en **[!UICONTROL Ver informe]** para ver el recorrido de una persona activa o finalizada y sus métricas de rendimiento y el flujo de actividad. Después de abrir el informe, puede seleccionar varios recorridos para incluirlos en él.

>[!PREREQUISITES]
>
>Para ver este informe, debe tener el **[!UICONTROL permiso de [Ver informes de Recorrido de personas B2B](../start/permissions-reference.md)]**.

_Para ver el informe :_

1. Abra un recorrido de **[!UICONTROL Live]** o **[!UICONTROL Finalizado]** personas de la lista _[!UICONTROL recorridos de personas]_.
1. En el encabezado del recorrido, seleccione **[!UICONTROL Ver informe]**.

   ![Lienzo de recorrido de persona con el botón Ver informe resaltado en el encabezado del recorrido.](./assets/reports-person-journey-view-report.png){width="600" zoomable="yes"}

Puede [cambiar el intervalo de fecha](./reports-overview.md#change-the-date-range) para el informe.

Seleccione **[!UICONTROL Compartir]** en la parte superior del informe para descargar o programar una exportación de los datos. Consulte [_Exportar un informe_](./reports-overview.md#export-a-report) en la descripción general de informes.

![Informe individual de Recorrido de persona con filtros de Nombre de Recorrido (evento) y Persona (evento) por encima del estado de recorrido, la tendencia de finalización y los mosaicos de participación.](./assets/reports-individual-journey.png){width="700" zoomable="yes"}

## Filtros {#filters}

El informe muestra inicialmente el recorrido desde el que lo abrió. Utilice los filtros de la parte superior del informe para cambiar los recorridos y los perfiles que se incluyen.

* **[!UICONTROL Nombre de Recorrido (evento)]**: preestablecido en el recorrido desde el que abrió el informe. Abra la lista de filtros y seleccione los recorridos que desea incluir. Puede seleccionar varios recorridos.
* **[!UICONTROL Persona (evento)]**: filtra el informe a las personas que coincidan con un [personaje derivado](../audiences/personas.md#filter-by-derived-persona) específico. El valor predeterminado es [!UICONTROL Sin filtro].

![Informe de Recorrido de personas con la lista de filtros de nombre de Recorrido (evento) abierta y tres recorridos seleccionados, junto con el filtro Persona (evento).](./assets/reports-person-journey-details-filters.png){width="700" zoomable="yes"}

Para filtrar por persona, abra la lista de filtros **[!UICONTROL Persona (evento)]** en la parte superior del informe y seleccione los valores que desea incluir.

Seleccione **[!UICONTROL Restablecer todo]** para restablecer los filtros del informe.

## Estado y participación de la persona {#person-status-and-engagement}

Esta sección presenta cuatro mosaicos:

* **[!UICONTROL Estado de las personas en el recorrido]**: desglosa las personas en el recorrido en las categorías _[!UICONTROL Completadas]_ y _[!UICONTROL En curso]_, con los porcentajes correspondientes.
* **[!UICONTROL Personas completadas a lo largo del tiempo]**: un gráfico de líneas que registra el número de personas que completaron el recorrido en el intervalo de fechas seleccionado.
* **[!UICONTROL Personas comprometidas y no comprometidas]**: desglosa las personas del recorrido en las categorías _[!UICONTROL Comprometidas]_ y _[!UICONTROL No comprometidas]_, con los porcentajes correspondientes.
* **[!UICONTROL Personas comprometidas]**: el número total de personas que cumplen los requisitos para participar en el recorrido.

## Rendimiento del correo electrónico {#email-performance}

La tabla [!UICONTROL Rendimiento del correo electrónico] muestra las métricas de envío y participación de cada correo electrónico enviado en el recorrido. Para las mismas métricas de correo electrónico en todos los recorridos, consulte el [informe de participación en el correo electrónico](./email-engagement-report.md).

![Tabla de rendimiento del correo electrónico que muestra las métricas enviadas, enviadas, abiertas y en las que se hizo clic para tres correos electrónicos.](./assets/reports-individual-journey-email-performance.png){width="700" zoomable="yes"}

[!UICONTROL Rendimiento de correo electrónico] columnas de tabla:

* [!UICONTROL Nombre de correo electrónico] - Nombre del correo electrónico.
* [!UICONTROL Enviado] - Número de correos electrónicos enviados.
* [!UICONTROL Entregado]: número de correos electrónicos entregados.
* [!UICONTROL % Entregado]: número de correos electrónicos entregados dividido por el número enviado.
* [!UICONTROL Abierto]: número de veces que los destinatarios abrieron el correo electrónico.
* [!UICONTROL % abierto] - Número de correos electrónicos abiertos dividido por el número de envíos.
* [!UICONTROL Se hizo clic] - Cantidad de veces que los destinatarios hicieron clic en un vínculo del correo electrónico.
* [!UICONTROL % hizo clic] - Número de correos electrónicos en los que se hizo clic dividido por el número de envíos.

## flujo de actividad de recorrido {#journey-activity-flow}

La visualización de [!UICONTROL flujo de actividad de Recorrido] muestra la ruta que las personas siguen a través del recorrido, a partir de la actividad _[!UICONTROL Agregar persona al Recorrido]_. Cada nodo muestra el número de vistas de esa actividad.

![Visualización del flujo de actividad de Recorrido que muestra las vistas de ruta desde Agregar persona a Recorrido a través de Enviar correo electrónico y las actividades de devolución de correo electrónico.](./assets/reports-individual-journey-activity-flow.png){width="500" zoomable="yes"}
