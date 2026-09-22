---
title: Informe individual de Recorrido de persona
description: Obtenga información acerca del informe Individual de Recorrido de persona en Adobe Marketo Optimizer, que muestra las métricas de finalización, participación y correo electrónico de un recorrido.
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
source-git-commit: 531dce4ffe6000efa0296f0e2393423f54124ea7
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%
---

# Informe Individual de Recorrido de persona

<!-- SPHR-39120: UX plans to move the Journey activity flow tile to the top of the report. Update the tile order in this page when that ships. -->

Haga clic en **[!UICONTROL Ver informe]** para ver el recorrido de una persona activa o finalizada y ver su rendimiento, incluido el estado, la participación, las métricas de correo electrónico y el flujo de actividad.

_Para ver el informe :_

1. Abra un recorrido de **[!UICONTROL Live]** o **[!UICONTROL Finalizado]** personas de la lista _[!UICONTROL recorridos de personas]_.
1. En el encabezado del recorrido, seleccione **[!UICONTROL Ver informe]**.

   ![Lienzo de recorrido de persona con el botón Ver informe resaltado en el encabezado del recorrido.](./assets/reports-person-journey-view-report.png){width="600" zoomable="yes"}

Puede [cambiar el intervalo de fecha](./reports-overview.md#change-the-date-range) para el informe.

Seleccione **[!UICONTROL Compartir]** en la parte superior del informe para descargar o programar una exportación de los datos. Consulte [_Exportar un informe_](./reports-overview.md#export-a-report) en la descripción general de informes.

![Informe individual de Recorrido de persona que muestra el estado de recorrido, la tendencia de finalización y los mosaicos de participación.](./assets/reports-individual-journey.png){width="700" zoomable="yes"}

## Filtros {#filters}

Los filtros de informe se vinculan al recorrido actual.

* **[!UICONTROL Nombre de Recorrido (evento)]**: preestablecido en el recorrido desde el que abrió el informe.
* **[!UICONTROL Persona (evento)]** - (_Aún no se admite_) Filtre el informe a las personas que coincidan con un [personaje derivado](../audiences/personas.md#filter-by-derived-persona) específico. El valor predeterminado es [!UICONTROL Sin filtro].

Seleccione **[!UICONTROL Restablecer todo]** para borrar el filtro _[!UICONTROL Persona (evento)]_ y volver a la vista predeterminada.

## Estado y participación de la persona {#person-status-and-engagement}

Esta sección presenta cuatro mosaicos:

* **[!UICONTROL Estado de las personas en el recorrido]**: desglosa las personas en el recorrido en las categorías _[!UICONTROL Completadas]_ y _[!UICONTROL En curso]_, con los porcentajes correspondientes.
* **[!UICONTROL Personas completadas a lo largo del tiempo]**: un gráfico de líneas que registra el número de personas que completaron el recorrido en el intervalo de fechas seleccionado.
* **[!UICONTROL Personas comprometidas y no comprometidas]**: desglosa las personas del recorrido en las categorías _[!UICONTROL Comprometidas]_ y _[!UICONTROL No comprometidas]_, con los porcentajes correspondientes.
* **[!UICONTROL Personas comprometidas]**: número total de personas que cumplen los requisitos para participar en el recorrido.

## Rendimiento del correo electrónico {#email-performance}

La tabla [!UICONTROL Rendimiento del correo electrónico] muestra las métricas de envío y participación de cada correo electrónico enviado en el recorrido. Para las mismas métricas de correo electrónico en todos los recorridos, consulte el [informe de participación en el correo electrónico](./email-engagement-report.md).

![Tabla de rendimiento del correo electrónico que muestra las métricas enviadas, enviadas, abiertas y en las que se hizo clic para un correo electrónico.](./assets/reports-individual-journey-email-performance.png){width="700" zoomable="yes"}

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

La visualización de [!UICONTROL flujo de actividad de Recorrido] muestra la ruta que las personas siguen a través del recorrido, a partir de la actividad _[!UICONTROL Agregar persona al Recorrido]_. Cada nodo muestra el número de vistas de ruta para esa actividad.

![Visualización del flujo de actividad de Recorrido que muestra las vistas de ruta desde Agregar persona al recorrido a través de la entrega de correo electrónico.](./assets/reports-individual-journey-activity-flow.png){width="700" zoomable="yes"}
