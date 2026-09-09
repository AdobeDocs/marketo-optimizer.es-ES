---
title: Configuración de Forms
description: Marcador de posición
TQID: 'https://experienceleague.adobe.com/7X5-67hfrjRjWbGjq9duLu7mVjgfCs7tpAQLV8u6YKE'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: a659ad61-de21-559d-a901-02e2fb329ff5id: d4203578-d294-5145-b397-f26f4488a904
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 541
ht-degree: 16%

---

# Configuraciones de Forms

Para que los especialistas en marketing puedan crear y publicar formularios para utilizarlos en sus páginas de aterrizaje, un administrador de productos debe crear uno o más ajustes preestablecidos dedicados. Cada ajuste preestablecido define el extremo de conexión utilizado para enviar los datos de envío del formulario y el conjunto de datos utilizado para almacenar los datos capturados.

Cuando los datos aterrizan en el extremo de flujo continuo, se vinculan con la información del conjunto de datos. Mediante las conexiones de origen/destino generadas y el flujo de origen, los datos se insertan en el conjunto de datos.

>[!BEGINSHADEBOX]

## Requisitos previos

Para usar formularios web, debes tener una o más _**conexiones de streaming de API HTTP**_ definidas en Adobe Experience Platform. Asegúrese de que cada conexión que desea utilizar cumple los siguientes requisitos:

* El tipo de datos debe establecerse en XDM (no en datos sin procesar)
* La autenticación debe estar deshabilitada (conexión no autenticada)

Para obtener información detallada sobre cómo crear conexiones de origen de flujo continuo, consulte la [_documentación de Experience Platform_](https://experienceleague.adobe.com/es/docs/experience-platform/sources/ui-tutorials/create/streaming/http).

<!-- 
permissions coming in GA

Forms channel configuration in Journey Optimizer B2B Edition requires the following [permissions](../start/user-management.md#b2b-product-permissions):

* _[!UICONTROL B2B Channel Configurations]_ > _[!UICONTROL View Forms Presets]_ - Required to view forms preset configurations.
* _[!UICONTROL B2B Channel Configurations]_ > _[!UICONTROL Manage Forms Presets]_ - Required to create, update, and delete forms preset configurations.
* _[!UICONTROL B2B Channel Configurations]_ > _[!UICONTROL Publish Forms Presets]_ - Required to publish forms preset configurations.
-->

>[!ENDSHADEBOX]

## Directrices de configuración de formularios preestablecidos

Al crear un ajuste preestablecido:

* Puede configurar varios ajustes preestablecidos utilizando diferentes combinaciones de conjuntos de datos y conexiones de flujo continuo.

* Puede reutilizar el mismo conjunto de datos o conexión de flujo continuo en varios ajustes preestablecidos.

* Cada conexión de flujo continuo genera automáticamente recursos como, por ejemplo:

  * _Conexión de Source_ - donde se originan los datos.
  * _Conexión de destino_ - donde se almacenan o consumen los datos.
  * _Flujo de Source_: la canalización que mueve datos de la conexión de origen a Experience Platform. Gestiona la asignación, la transformación y la validación.

## Crear un ajuste preestablecido de un formulario {#create-preset}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_form_connection"
>title="Seleccione el punto final que desea utilizar"
>abstract="Defina el punto final de streaming al que se envían los datos al enviar el formulario."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-platform/sources/ui-tutorials/create/streaming/http" text="Crear una conexión de streaming de la API HTTP"

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_form_dataset"
>title="Selección de un conjunto de datos"
>abstract="Defina un conjunto de datos en el que se almacenan y reflejan las respuestas del formulario. Escriba texto si desea buscar un conjunto de datos específico o seleccionarlo en la lista."

1. En el panel de navegación izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]**.

1. En _[!UICONTROL Configuración de formulario]_ en el panel de navegación, seleccione **[!UICONTROL Ajustes preestablecidos de formulario]**.

   <!-- ![Access the form configurations](./assets/config-channels-forms.png){width="800" zoomable="yes"} -->

1. Haga clic en **[!UICONTROL Crear ajuste preestablecido de formulario]**.

1. Escriba un **[!UICONTROL Nombre]** único (obligatorio) y una **[!UICONTROL Descripción]** (opcional) para la configuración.

   >[!NOTE]
   >
   >Los nombres deben comenzar por una letra (A-Z) y solo pueden contener caracteres alfanuméricos. También puede utilizar caracteres de guion bajo `_`, punto `.` y guión `-`.

1. Seleccione la **[!UICONTROL conexión de transmisión]**.

   Esta conexión es el extremo de flujo continuo utilizado para enviar los datos cuando un visor web envía un formulario. Si la conexión de flujo continuo necesaria no aparece en la lista, compruebe que se cumplen los requisitos.

1. Haga clic en el icono _Seleccionar conjunto de datos_ ( ![Seleccionar icono del conjunto de datos](../assets/do-not-localize/icon-select-data.svg) ) para vincular un conjunto de datos con el formulario.

   En el conjunto de datos es donde se almacenan y reflejan las respuestas del formulario. Puede introducir una cadena de texto para buscar un conjunto de datos específico o seleccionarlo en la lista.

   <!-- ![Select datasets dialog](./assets/config-channel-forms-select-datasets.png){width="500" zoomable="yes"} -->

   >[!NOTE]
   >
   >Actualmente, solo se pueden seleccionar [conjuntos de datos de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/catalog/datasets/overview) habilitados para perfiles y no habilitados para perfiles. Puede seleccionar un conjunto de datos a la vez. Los conjuntos de datos del sistema no se pueden usar para guardar datos de formulario.

   Seleccione la casilla de verificación del conjunto de datos y haga clic en **[!UICONTROL Seleccionar]**.

1. Haga clic en **[!UICONTROL Guardar como borrador]**.

## Publicar un ajuste preestablecido de formulario

1. Haga clic en el nombre del ajuste preestablecido del formulario para abrir la página de configuración.

   Si es necesario, puede realizar los ajustes necesarios en el borrador.

1. Haga clic en **[!UICONTROL Publicar]**.

   Cuando el ajuste preestablecido del formulario aparece en la lista con el estado _Publicado_, está disponible para su uso durante la creación del formulario.
