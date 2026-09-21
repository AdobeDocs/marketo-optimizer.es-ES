---
title: Informes
description: Comprenda la pestaña Informes en Adobe Marketo Optimizer, incluidas sus secciones de informes, las opciones de exportación y programación, y cómo cambiar el intervalo de fechas.
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
source-git-commit: 6e919a66af259ea1f5facf7f5c3e811d76101e85
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 2%
---

# Informes

La ficha [!UICONTROL Informes] le proporciona información sobre el rendimiento de [!DNL Adobe Marketo Optimizer], incluido el compromiso del recorrido, el rendimiento del correo electrónico y la actividad web. En el panel de navegación izquierdo, seleccione **[!UICONTROL Informes]** para abrirlo.

Cada informe se genera en [!DNL Adobe Customer Journey Analytics] y se incrusta directamente en [!DNL Marketo Optimizer]. Haga clic en el icono _Lista_ ( ![Icono de lista](../assets/do-not-localize/icon-table-of-contents.svg) ) para usar el panel **[!UICONTROL Tabla de contenido]** de la izquierda para saltar entre secciones.

![La página Informes enumera las secciones Información general del Recorrido de persona, Participación, Participación por correo electrónico y Participación en la web](./assets/reports-table-of-contents.png){width="800" zoomable="yes"}

## Secciones del informe {#report-sections}

La ficha [!UICONTROL Informes] organiza los informes generados previamente en cuatro secciones. Cada sección tiene uno o más elementos descargables y su propia página de documentación con detalles sobre sus métricas y visualizaciones.

| Sección | Elementos descargables | Página de informe |
| --- | --- | --- |
| [!UICONTROL Información general sobre el Recorrido de personas] | Número de recorridos activos | [Informe de información general sobre el Recorrido de personas](./person-journey-overview-report.md) |
| [!UICONTROL Participación] | Participación de las personas, participación de las personas a lo largo del tiempo | [Informe de interacción](./engagement-report.md) |
| [!UICONTROL Participación por correo electrónico] | Participación por correo electrónico | [Informe de participación por correo electrónico](./email-engagement-report.md) |
| [!UICONTROL Participación en la web] | Vistas de la página principal | [Informe de participación en la web](./web-engagement-report.md) |

## Informes de registro individual {#individual-record-reports}

Algunos informes se centran en un único registro en lugar de en una vista de toda la sección y se accede a ellos desde un área diferente de la aplicación.

* Para obtener rendimiento de optimización del tiempo de envío de correo electrónico, abra el informe desde la interfaz de chat de [!UICONTROL Coworker]. Para ver los pasos, consulte [Optimización del tiempo de envío de correo electrónico](../marketing/email-send-time-optimization.md#reporting).
* Para el progreso de una persona a través de un solo recorrido, abra el [informe individual de Recorrido de persona](./person-journey-individual-report.md) desde ese recorrido.

## Exportación de informes {#export-a-report}

Seleccione **[!UICONTROL Compartir]** en la parte superior de la página del informe para exportar o programar la entrega de sus datos.

![Compartir el menú con las opciones Descargar CSV, Descargar PDF, Programar exportación y Administrar programaciones](./assets/reports-share-menu.png){width="500"}

* **[!UICONTROL Descargar CSV]**: exporte los datos del informe como valores de texto sin formato.

* **[!UICONTROL Descargar PDF]**: exporte todas las tablas y visualizaciones visibles en el informe como un archivo PDF.

* **[!UICONTROL Exportación programada]**: configure una exportación recurrente del informe, que se enviará semanal o mensualmente como archivo CSV o PDF.

* **[!UICONTROL Administrar programaciones]**: revise y administre las exportaciones programadas existentes. La opción muestra un recuento en ejecución, como `3/10`, de las programaciones utilizadas en relación con el límite de su organización.

>[!NOTE]
>
>Su organización puede tener un máximo de 10 exportaciones programadas en todos los informes, con frecuencia semanal o mensual. Si no es administrador, solo puede administrar sus propias exportaciones programadas. Los administradores pueden ver y administrar todas las exportaciones programadas en la organización.

## Analizar un informe en [!DNL Customer Journey Analytics] {#analyze-a-report-in-cja}

>[!AVAILABILITY]
>
>Esta función está disponible si su organización dispone de licencia para [!DNL Adobe Customer Journey Analytics] y se le ha asignado el perfil de producto.

Seleccione **[!UICONTROL Analizar en CJA]** en cualquier sección del informe para abrirlo en [!DNL Adobe Customer Journey Analytics] Workspace, donde podrá crear visualizaciones personalizadas además de las que están disponibles en el informe incrustado.

## Cambio del intervalo de fecha {#change-the-date-range}

Cada sección del informe muestra los datos de un intervalo de fechas específico, en la esquina superior derecha de la sección. Haga clic en los campos de intervalo de fechas para mostrar las herramientas de selección de fechas y seleccionar el intervalo de fechas. Puede elegir un ajuste preestablecido diferente o definir un intervalo personalizado.

![Selector de intervalo de fechas con un calendario de dos meses, campos de fecha de inicio y finalización y opciones preestablecidas](./assets/reports-date-range.png){width="600"}
