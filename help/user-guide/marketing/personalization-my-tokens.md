---
title: Tokens personalizados para Personalization
description: Cree y administre mis tokens personalizados para la personalización dinámica de sus artefactos de marketing . Defina variables de texto y números para los programas en Marketo Optimizer.
TQID: 'https://experienceleague.adobe.com/utVM69g7aQSuF-V3XQIdVBqvBXyiDz1ZWr0WtE67UCg'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
    internal-label: Journeys
  - id: a29661b8-f7a4-53d1-a9ac-fdec08c092e4
    internal-label: Programs
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 177e7c3d0806febd730104b19787ba3cbea2914a
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 3%
---
# Tokens personalizados para personalización

La personalización de contenido utiliza tokens como marcadores de posición o variables que se rellenan cuando se genera el artefacto de contenido. Los tokens de personalización estándar están disponibles para correos electrónicos, páginas de aterrizaje, fragmentos y plantillas. También puede definir un conjunto de tokens personalizados con valores específicos del programa o la carpeta. Este conjunto de tokens personalizados se denomina _Mis tokens_ y cualquiera de ellos está disponible para personalización.

<!-- 
When you add a custom token to an email, it is displayed as `{{my.TokenName}}`. For example, you might have `{{my.EventDate}}` or `{{my.WebinarSpeaker}}` tokens created to manage email content related to upcoming webinars in your program.
-->

Además de _Mis tokens_, que son específicos del programa o la carpeta, puede usar cualquiera de los tokens estándar (integrados) para la personalización.

>[!IMPORTANT]
>
>Para la versión inicial de Marketo Optimizer, _Mis tokens_ son compatibles con los nodos de acción Cambiar valor de datos del recorrido y están limitados a su uso en atributos de cadena y texto. _Mis tokens_ no están **habilitados** actualmente en el editor de Personalization.

## Tokens de acceso {#access-tokens}

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Administración de mercadotecnia]**.

1. A la derecha de la lista de recursos de **[!UICONTROL Marketing]**, seleccione **[!UICONTROL Programas]**.

1. En la estructura de árbol, seleccione el programa o la carpeta para abrir los detalles en el espacio de trabajo central.

1. Haga clic en la ficha **[!UICONTROL Tokens]**.

   ![Ficha Tokens en el programa seleccionado](./assets/program-tokens-tab.png){width="800" zoomable="yes"}

   La pestaña muestra todos los tokens personalizados definidos dentro de la carpeta o programa, así como cualquier token definido para carpetas o programas principales.

### Tipos de token {#my-tokens}

Los _Mis tokens_ son variables personalizadas que se crean o modifican para un programa o carpeta. Este conjunto de tokens personalizados admite los siguientes tipos de tokens:

| Tipo de token | Descripción |
| ---------- | ----------- |
| Texto | Este tipo contiene una cadena de texto estándar. El límite de tamaño para los tokens de texto es de 524 288 caracteres (UTF-8) o 2 MB. |
| Fecha | Este tipo contiene un valor de fecha. La fecha se muestra como mes-día-año (por ejemplo, 23-9-2026). |
| Fecha y hora | Este tipo contiene un valor de fecha y hora. |
| Número | Este tipo contiene un valor entero estándar. |
| Correo electrónico | Este tipo contiene una dirección de correo electrónico válida. |
| Puntuación | Utilice este token para cambiar la puntuación de un nodo de acción de recorrido. |
| Booleano | Este tipo contiene un valor booleano estándar, true o false. |
| Texto enriquecido | Este tipo contiene texto con formato. |

### Anidado de tokens {#nesting}

Cuando se crea un token en un programa o una carpeta, está disponible para referencia por objetos dentro de la jerarquía.

* **Token local**: el token se define en el mismo programa o carpeta.
* **Token heredado**: el token se define en un programa o carpeta principal, uno o más niveles por encima del programa o carpeta actual.
* **Token anulado**: el token se define en un programa o carpeta principal, pero se define un valor diferente en el programa o carpeta actual. El estado del token cambia a _Anulado_, y todas las carpetas, programas y artefactos de marketing secundarios heredan el nuevo valor.

![Tipos de tokens y herencia](./assets/program-tokens-inherited-overridden.png){width="600" zoomable="yes"}

### Crear un token {#create}

1. En la ficha _[!UICONTROL Tokens]_, haga clic en **[!UICONTROL Crear]**.

1. En el cuadro de diálogo, escriba el **[!UICONTROL Nombre]** para el token.

   ![Escriba un nombre y un valor para el token de texto](./assets/token-create-dialog.png){width="400"}

   No se pueden utilizar espacios ni caracteres especiales en el nombre del token. Puede usar _minúscula_, como `EventType`, para usar un nombre de varias palabras que se identifique fácilmente.

1. Elija **[!UICONTROL Type]** para el token.

1. Establezca **[!UICONTROL Value]** para el token.

1. Haga clic en **[!UICONTROL Crear]**.

### Edición de un token {#edit}

Puede editar el valor de cualquiera de los Mis tokens definidos, que anulan el valor de un token heredado.

<!-- (How does this affect live person journeys? ) -->

1. En _[!UICONTROL Tokens]_ , haga clic en el icono _Editar_ junto al nombre del token.

1. En el campo, cambie el valor según sea necesario.

   ![Cambiar el nombre y el valor del token](assets/my-tokens-edit-text-token-dialog.png){width="400"}

1. Haga clic en el icono _Guardar_.

### Eliminación de un token {#delete}

Puede eliminar un token personalizado de la lista si actualmente no se utiliza en el contenido del correo electrónico de recorrido.

1. En _[!UICONTROL Tokens]_ , haga clic en el icono _Delete_ junto al nombre del token.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.

## Sugerencia y previsualización automáticas {#autosuggest}

Cuando incluya un _Cambiar valor de datos_ [nodo de acción](./action-nodes.md) en el recorrido, puede escribir `{{` en el campo **[!UICONTROL Nuevo valor]** para mostrar el menú de tokens _Sugerir automáticamente_. La lista mostrada muestra áreas de nombres compatibles y tokens individuales. Solo se muestran los tokens de un tipo de datos compatible.

Para _Mis tokens_, se muestra una vista previa del valor del token con el nombre del token para facilitar la selección del valor correcto.

![Sintaxis en el campo Nuevo valor para mostrar el menú de sugerencias automáticas para tokens](./assets/program-tokens-change-data-value-autosuggest.png){width="500" zoomable="yes"}

<!--

## Use custom tokens in your content

When you are authoring email content for your programs, you can use any of the tokens from the _My Tokens_ list when you use the personalization tools in the visual design space.

1. Select the text component and click the _Add personalization_ ( ![Add personalization icon](../assets/do-not-localize/icon-personalization-field.svg) ) icon in the toolbar.

   ![Click the Add personalization icon](assets/email-personalize-text.png){width="600"}

   This action opens the _Edit Personalization_ dialog. The dialog includes a _[!UICONTROL My tokens]_ folder in the _[!UICONTROL Personalization Tokens]_ library if there are custom tokens defined for the account journey.

1. To add one of your custom tokens to the blank space, expand the **[!UICONTROL My tokens]** folder, then click **+** or **...**.

   You can add any additional static text as needed.

   ![Construct personalized text using My tokens](assets/personalization-edit-dialog-my-tokens.png){width="700" zoomable="yes"}

1. Click **[!UICONTROL Save]**.

-->
