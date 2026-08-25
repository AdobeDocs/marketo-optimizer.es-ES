---
title: Editor de Personalization
description: Aprenda a utilizar el editor de personalización en Marketo Optimizer para seleccionar, organizar, personalizar y validar tokens de atributos de perfil en correos electrónicos, mensajes de WhatsApp, páginas de aterrizaje y campos de URL.
feature: Content Design Tools
role: User
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 12%

---

# Editor de personalización

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_personalization_editor"
>title="Acerca del editor de personalización"
>abstract="El editor de personalización permite seleccionar, organizar, personalizar y validar los atributos de perfil para crear contenido personalizado."

El editor de personalización es la pieza central de la personalización en [!DNL Marketo Optimizer]. Utilícelo dondequiera que necesite contenido dinámico: en correos electrónicos, mensajes de WhatsApp, páginas de aterrizaje y campos de URL.

En la interfaz del editor de personalización, puede seleccionar, organizar, personalizar y validar atributos de perfil para crear contenido personalizado.

![Editor de expresiones de personalización](./assets/personalization-editor.png){width="700" zoomable="yes"}

>[!NOTE]
>
>En esta versión de Beta, solo los atributos de perfil están disponibles en el editor de personalización. La personalización de nivel de cuenta y los datos de objetos personalizados no están disponibles. Ver [limitaciones actuales](../marketing/email-channel.md#limitations).

Puede agregar personalización en cualquier campo con el icono _Personalizar_ ( ![Icono Personalizar](../assets/do-not-localize/icon-personalize.svg) ). Expanda las siguientes secciones para obtener más detalles.

+++Correos electrónicos y mensajes de WhatsApp

En [correos electrónicos](./email-authoring.md#personalize-content) y [mensajes de WhatsApp](./whatsapp-authoring.md#personalize-message-content), se puede agregar personalización en diferentes ubicaciones, como el campo **[!UICONTROL Línea de asunto]** de un correo electrónico o parámetros dinámicos en una plantilla de WhatsApp aprobada.

También se puede añadir en otras secciones del contenido, incluido el texto del cuerpo del correo electrónico, los encabezados previos y las direcciones URL de los botones.

+++

+++Espacio de diseño de contenido

Al editar contenido visual, puede añadir personalización en la mayoría de los elementos de texto mediante el icono de la barra de herramientas contextual.

<!-- ![](assets/perso_insert.png) -->

+++

+++URL

[!DNL Marketo Optimizer] también le permite personalizar **direcciones URL** en sus mensajes. Las direcciones URL personalizadas llevan a los destinatarios a páginas específicas de un sitio web o a un micrositio personalizado, según los atributos del perfil.

<!-- ![](assets/perso-url.png){width="50%"} -->

>[!NOTE]
>
>La personalización de URL está disponible para estos tipos de vínculos: **Vínculo externo**, **Vínculo de baja** y **Exclusión**.

+++

+++Configuración de correo electrónico

Al crear una [configuración de canal de correo electrónico](../admin/email-channel-configuration.md), puede definir valores personalizados para subdominios, encabezados y parámetros de seguimiento de URL.

+++

## Añadir personalización {#add}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_perso_editor_autocomplete"
>title="Autocompletar"
>abstract="Al activar esta opción el sistema sugiere y completa automáticamente el código mientras se escribe. Esta función solo está disponible en los formatos HTML y texto, y admite atributos de perfil. Si se desactiva mediante el conmutador, el editor proporcionará el relleno automático de código HTML nativo en su lugar."

En el espacio de trabajo central se crea la sintaxis de personalización. Para utilizar un atributo para personalizar el mensaje, localícelo en el panel de navegación izquierdo y haga clic en el botón `+` para agregarlo a la expresión.

<!-- ![](assets/personalization-add-attribute.png) -->

El menú de los tres puntos situado junto al icono `+` le permite obtener más información sobre cada atributo y agregar a los favoritos los atributos utilizados con más frecuencia. Se puede acceder a los atributos agregados a favoritos desde el menú **[!UICONTROL Favoritos]** del panel de navegación.

>[!NOTE]
>
>De forma predeterminada, el panel Atributos solo muestra los atributos rellenados. Para mostrar todos los atributos, seleccione el botón **[!UICONTROL Configuración]** en el panel de atributos y desactive la opción **[!UICONTROL Mostrar solo atributos rellenados]**.

Además, puede definir el texto de reserva predeterminado que se mostrará si un atributo de perfil de tipo cadena está vacío. Para ello, haga clic en el botón de puntos suspensivos situado junto al atributo y seleccione **[!UICONTROL Insertar con texto de reserva]**. Escriba el texto que debería mostrarse de forma predeterminada si el valor del atributo está vacío para un perfil y, a continuación, haga clic en **[!UICONTROL Agregar]**.

<!-- ![](assets/attribute-details.png) -->

Por ejemplo, puede saludar a cada destinatario por su nombre utilizando `{{profile.firstName}}` con una reserva cuando falte el valor: `{{profile.firstName | default: "there"}}`.

## Opciones para la edición de expresiones {#options}

El espacio de trabajo central proporciona varias herramientas para ayudarle a escribir su expresión de personalización.

<!-- ![](assets/perso-workspace.png) -->

Entre las opciones disponibles se encuentran:

1. **[!UICONTROL Buscar]** / **[!UICONTROL Buscar y reemplazar]**: Busca a través de tu expresión y reemplaza automáticamente partes de código.
1. **[!UICONTROL Deshacer]** / **[!UICONTROL Rehacer]**: Deshacer / Rehacer la última operación.
1. **[!UICONTROL Completar automáticamente]**: sugiere y completa automáticamente el código mientras escribe. Esta función solo está disponible en los formatos HTML y texto, y admite atributos de perfil. Si se desactiva mediante el conmutador, el editor proporcionará el relleno automático de código HTML nativo en su lugar.

   <!-- ![](assets/perso-complete.png){width="70%" align="center" zoomable="yes"} -->

1. **[!UICONTROL HTML]** / **[!UICONTROL JSON]** / **[!UICONTROL Text]**: identifique el formato de su código. Esto permite al sistema adaptar la función de validación y autocompletar en función del idioma seleccionado.
1. **[!UICONTROL Validar]**: compruebe la sintaxis de su expresión.
1. **[!UICONTROL Tamaño de fuente]**: Ajusta el tamaño de fuente del contenido dentro del editor para mejorar la legibilidad.
1. **[!UICONTROL Ajuste de palabras]**: habilita o deshabilita el ajuste de palabras, lo que permite que las expresiones largas se muestren en una sola línea o se ajusten dentro del editor. Las opciones incluyen:
   * **Desactivado** (Predeterminado) - Sin ajuste de palabras. Las líneas largas se extienden más allá de la vista del editor y requieren un desplazamiento horizontal.
   * **Activado**: ajusta líneas en la anchura del editor.
   * **Columna de ajuste de línea**: ajusta líneas cuando una línea alcanza los 80 caracteres.
   * **Redondeado**: ajusta las líneas en la anchura del editor o en 80 caracteres, el valor que sea menor.
1. **[!UICONTROL Pills]**: muestra los atributos como &quot;píldoras&quot; compactas para mejorar la legibilidad al ocultar rutas de atributos largas. Haga clic en un atributo para mostrar su ruta completa.

   >[!NOTE]
   >
   >Esta opción solo está disponible para atributos de perfil.

En el panel de navegación, hay disponibles funciones adicionales que le ayudarán a crear su expresión de personalización.

<!-- ![](assets/perso-features.png) -->

* **[!UICONTROL Funciones de ayuda]**: las funciones de ayuda le permiten realizar operaciones en los datos, como cálculos, conversiones o formato de datos, condiciones y manipularlos en el contexto de la personalización.

* **[!UICONTROL Favoritos]**: los atributos que agregó a los favoritos se muestran en esta lista. Esto le permite acceder rápidamente a los elementos utilizados con más frecuencia. Para agregar un atributo a tus favoritos, haz clic en el menú de los tres puntos y elige **[!UICONTROL Agregar a favoritos]**.

El colaborador puede generar expresiones Handlebars a partir de descripciones en lenguaje sencillo, explicar expresiones existentes e identificar posibles problemas.

Cuando la expresión personalizada esté lista, haz clic en **[!UICONTROL Confirmar]** o **[!UICONTROL Insertar]** para agregarla al contenido.

## Mecanismos de validación {#validation-mechanisms}

La validación de la expresión se ejecuta automáticamente al hacer clic en **[!UICONTROL Confirmar]** o **[!UICONTROL Insertar]** para cerrar el editor. También puede hacer clic en **[!UICONTROL Validar]** para comprobar la sintaxis de personalización antes de cerrar.

Para las alertas de contenido que bloquean la activación del recorrido, consulte [Validación del contenido del correo electrónico](./email-authoring.md#validation).

Expanda la siguiente sección para ver los errores comunes que pueden producirse al validar la personalización.

+++Errores comunes

* **No se encontró la ruta &quot;XYZ&quot;**

Este error se produce cuando se hace referencia a un campo que no está definido en el esquema.

En este caso **firstName1** no está definido como atributo en el esquema de perfil:

```handlebars
{{profile.firstName1}}
```

* **No coinciden los tipos para la variable &quot;XYZ&quot;. Matriz esperada. Se encontró la cadena.**

Este error se produce cuando se intenta repetir una cadena en lugar de una matriz.

En este caso **jobTitle** es una cadena, no una matriz:

```handlebars
{{#each profile.jobTitle as |item|}}
  {{item}}
{{/each}}
```

* **Sintaxis de handlebars no válida. Se encontró`'[XYZ}}'`**

Este error se produce cuando se utiliza una sintaxis de Handlebars no válida.

```handlebars
{{[profile.firstName}}
```

+++
