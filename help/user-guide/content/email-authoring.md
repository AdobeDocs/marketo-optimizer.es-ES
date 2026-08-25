---
title: Contenido de correo electrónico
description: Obtenga información sobre cómo componer y diseñar contenido de correo electrónico en Adobe Marketo Optimizer mediante el lienzo visual, las herramientas de arrastrar y soltar, la importación de HTML y las plantillas reutilizables.
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: '2287'
ht-degree: 2%

---

# Creación de contenido de correo electrónico

En [!DNL Adobe Marketo Optimizer], el espacio de diseño de correo electrónico proporciona un lienzo visual en el que los especialistas en marketing componen el correo electrónico. Las herramientas de diseño de correo electrónico de los paneles izquierdo y superior (estructuras, componentes de contenido, plantillas, fragmentos y mucho más) admiten la creación desde cero con la función de arrastrar y soltar. También puede elegir comenzar desde una plantilla, pegar HTML sin procesar o ensamblar mensajes a partir de fragmentos visuales reutilizables.

>[!IMPORTANT]
>
>Para obtener información sobre la configuración de administrador de subdominios, autenticación, grupos de IP y configuraciones de canales de correo electrónico, consulte [Capacidad de entrega de correos electrónicos](../start/email-deliverability.md) y [Configuración de canales de correo electrónico](../admin/email-channel-configuration.md).

En [!DNL Marketo Optimizer], cada correo electrónico está asociado con una acción _[!UICONTROL Enviar correo electrónico]_ dentro del recorrido de una persona. El flujo de trabajo completo, desde el diseño del recorrido hasta la definición de correo electrónico, se produce en una experiencia continua. Cuando [agregue un nodo _Enviar correo electrónico_](../marketing/action-nodes.md#add-an-action-node) al recorrido de una persona, haga clic en **[!UICONTROL Crear correo electrónico]** para iniciar el proceso. En primer lugar, defina las acciones y la configuración de contenido del correo electrónico. Haga clic en **[!UICONTROL Editar cuerpo del correo electrónico]** para iniciar el espacio de diseño del contenido del correo electrónico, donde puede elegir cómo desea diseñar el correo electrónico con las siguientes opciones:

* [Diseñe su correo electrónico desde cero](#design-from-scratch) con la interfaz de diseño visual. Cree el componente Diseño de correo electrónico mediante arrastrar y soltar en un lienzo en blanco. Este método es mejor para crear nuevas plantillas o correos electrónicos únicos.

* [Importe contenido existente de HTML](#import-html-content) en el editor de código o trabaje en paralelo con el lienzo visual.

* [Seleccione una plantilla existente](#templates) de una lista de plantillas de correo electrónico integradas o personalizadas. Este método es mejor para casos de uso de correo electrónico repetibles.

<!-- * Upload a design prototype (JPG, PNG, PDF, or Figma export) and have Coworker convert it into a responsive HTML email. (Image to HTML (Img2HTML) -->

![Crear su página de correo electrónico](./assets/email-design-create-your-email.png){width="800" zoomable="yes"}

## Herramientas de diseño de correo electrónico {#email-design-tools}

* **Barra de herramientas superior:** Guardar, Atrás, Cambiar al editor de código, controles de vista previa.
* **Panel izquierdo:** estructuras (diseños de columna), contenido (texto, botón, imagen, divisor, social, HTML), fragmentos, plantillas, árbol de navegación (jerarquía de estilo DOM del correo electrónico).
* **Lienzo central:** editor de WYSIWYG con vista previa para escritorio y móvil.
* **Panel derecho:** Configuración y estilos para el componente seleccionado actualmente, incluidas las propiedades de contenido, el fondo, el borde, el relleno y la personalización.

>[!BEGINSHADEBOX]

## Prácticas recomendadas para el diseño de correo electrónico {#design-best-practices}

Las siguientes prácticas recomendadas de HTML y CSS ayudan a garantizar un procesamiento coherente entre los clientes de correo electrónico.

| Enfoque | Guía |
| -------- | -------- |
| **Recomendado** | Diseños estáticos basados en tablas · Tablas HTML y tablas anidadas · Anchuras de plantilla de 600-800 px · CSS en línea simple · Fuentes seguras para la web |
| **Usar con cuidado** | Imágenes de fondo (compatibilidad limitada con el cliente) · Fuentes web personalizadas (defina siempre una fuente de reserva) · Diseños más anchos que 800 px · Mapas de imagen |
| **Evitar** | JavaScript, iframes o Flash · Audio o vídeo incrustados · Formularios HTML · Diseños basados en Div |

>[!NOTE]
>
>El contenido del correo electrónico también debe cumplir los requisitos de accesibilidad digital aplicables. Estructura los encabezados de forma lógica, proporciona texto alternativo para todas las imágenes y verifica el contraste de color en los modos claro y oscuro.

>[!ENDSHADEBOX]

## Diseñe el correo electrónico desde cero {#design-from-scratch}

Utilice el espacio de diseño de contenido visual para definir la estructura y el contenido del correo electrónico. Al añadir y mover componentes estructurales con sencillas acciones de arrastrar y soltar, puede diseñar el diseño y la organización del contenido del correo electrónico en cuestión de segundos.

1. En la página _[!UICONTROL Diseña tu correo electrónico]_, selecciona la opción **[!UICONTROL Diseñar desde cero]**.

<!-- 

1. In the _[!UICONTROL Create email]_ dialog, choose the type of email content that you want to author.

   * **[!UICONTROL Use Themes]** - Choose this option to create the email in _Theme mode_. In this mode, you can use a defined brand theme to streamline the content authoring process and make sure that the design aligns with defined standards.

   * **[!UICONTROL Manual Styling]** - Choose this option to create the email in _Manual mode_. In this mode, you manually set the styling for all structure and content components that you add to the blank canvas.

-->

1. [Agregar componentes de estructura y contenido](#structure-content) en el lienzo.

1. [Revisar y actualizar vínculos](#preview-and-edit-linked-urls).

1. [Probar el correo electrónico](#check-and-test-the-email).

Cuando esté satisfecho con el contenido, haga clic en **[!UICONTROL Guardar]**.

## Importar contenido existente de HTML {#import-html-content}

<!-- originally  from   /help/_includes/content-design-import.md but copied and revised to omit the part about Marketo Engage assets and AEM assets -->

El contenido importado puede ser:

* Archivo HTML con una hoja de estilos incorporada
* Archivo .zip que incluye un archivo HTML, la hoja de estilos (.css) y las imágenes

  >[!NOTE]
  >
  >No hay restricciones en la estructura de archivos .zip. Sin embargo, las referencias deben ser relativas y ajustarse a la estructura de árbol de la carpeta .zip. Las imágenes siempre se cargan en el [repositorio de recursos](./digital-asset-management.md).

_Para importar un archivo que contenga contenido de HTML :_

1. En la página de inicio de diseño, seleccione la opción **[!UICONTROL Importar HTML]**.

1. Arrastre y suelte el archivo HTML o .zip que contiene el contenido HTML y haga clic en **[!UICONTROL Importar]**.

![importar contenido html en un archivo zip](assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>El uso de una etiqueta `<table>` como primera capa de un archivo HTML puede causar la pérdida de estilo, incluida la configuración del fondo y el ancho en la etiqueta de la capa superior.

Puede personalizar el contenido importado según sea necesario con las herramientas visuales del editor de correo electrónico.

## Seleccionar una plantilla {#templates}

Cuando abra el espacio de diseño de correo electrónico, utilice la sección **[!UICONTROL Seleccionar plantilla de diseño]** para comenzar desde una plantilla de muestra integrada o una plantilla personalizada guardada. Consulte [Usar una plantilla en un correo electrónico](./templates.md#use-in-journey) para ver el flujo de trabajo completo.

>[!NOTE]
>
>Las plantillas guardadas pueden tener configuraciones de gobernanza (bloqueo de contenido) aplicadas a uno o varios componentes. El espacio de diseño visual proporciona directrices sobre los componentes bloqueados cuando [crea un correo electrónico a partir de una plantilla controlada](./template-content-governance.md).

## Añadir estructura y contenido {#structure-content}

Utilice el editor visual de correo electrónico para crear el mensaje de correo electrónico. Añada un preencabezado, estructure el diseño con columnas y divisores y, a continuación, rellene esas estructuras con componentes de contenido como imágenes, botones y texto. También puede aplicar CSS personalizado para un estilo avanzado y previsualizar cómo se procesa el diseño en modo oscuro.

### Establecer el encabezado previo {#preheader}

El preencabezado es el fragmento de texto que se muestra después de la línea de asunto en las vistas previas de la bandeja de entrada. En [!DNL Marketo Optimizer], el preencabezado se configura en el lienzo visual en el espacio de diseño del correo electrónico, no en la pantalla de propiedades de correo electrónico junto a la línea de asunto.

Con el **[!UICONTROL Cuerpo]** seleccionado en el árbol de navegación izquierdo, abre el panel **[!UICONTROL Configuración]** a la derecha.

Haga clic en la región de texto **[!UICONTROL Preheader]** e introduzca su copia de preencabezado. Haga clic en el icono _Agregar personalización_ (![Agregar icono de personalización](../assets/do-not-localize/icon-personalization-field.svg) ) para aplicar formato y [tokens de personalización](#personalize-content) según sea necesario utilizando los controles de texto enriquecido.

>[!TIP]
>
>Mantenga el encabezado previo entre 40 y 100 caracteres. Debe complementar la línea de asunto (no repetirla) y dar al destinatario un motivo adicional para abrir el correo electrónico.

### Modo oscuro {#dark-mode}

Se admite el procesamiento en modo oscuro mediante consultas de medios CSS `prefers-color-scheme`. Las herramientas de diseño de correo electrónico incluyen una previsualización en modo oscuro y opciones para definir un estilo personalizado para los clientes de correo electrónico, lo que le ayuda a validar que el texto sigue siendo legible, que los logotipos son visibles y que los colores de la marca se mantienen contra fondos oscuros.

Para obtener instrucciones detalladas sobre la vista previa, la configuración del modo oscuro personalizado, la compatibilidad con clientes de correo electrónico y las prácticas recomendadas de prueba, consulte [Modo oscuro para el contenido de correo electrónico](./email-dark-mode.md).

### Adición de componentes de estructura y contenido {#components}

Cree su diseño de correo electrónico agregando [componentes de estructura](./structure-components.md) y [componentes de contenido](./content-components.md) al lienzo.

Arrastre elementos de las secciones **[!UICONTROL Structures]** y **[!UICONTROL Contents]** del panel izquierdo y, a continuación, configure cada componente en las pestañas _[!UICONTROL Settings]_ y _[!UICONTROL Styles]_ de la derecha.

### Añadir CSS personalizado {#custom-css}

Puede añadir CSS personalizado directamente en el espacio de diseño de correo electrónico para un estilo avanzado más allá de la configuración de componentes estándar. Se recomienda añadir este estilo de nivel superior antes de incluir componentes de contenido, como imágenes, botones y texto.

Consulte [Agregar CSS personalizado para el contenido](./design-custom-css.md) para ver los pasos, las reglas de sintaxis y la solución de problemas.

>[!NOTE]
>
>Si el mensaje de correo electrónico está diseñado con una [plantilla con contenido bloqueado](./template-content-governance.md), no podrá agregar CSS personalizado al contenido. La etiqueta del botón cambia a **[!UICONTROL Ver CSS personalizado]** y cualquier CSS personalizado que ya esté presente en el contenido es de solo lectura.

### Añadir fragmentos {#visual-fragments}

Un fragmento visual es un componente de diseño reutilizable al que varios recursos de contenido de [!DNL Marketo Optimizer] pueden hacer referencia. Normalmente es un bloque de contenido que se puede crear previamente e insertarse rápidamente para que la creación sea más rápida y coherente.

En el siguiente ejemplo se describen los pasos para agregar fragmentos a medida que crea el contenido.

1. Para abrir la lista de fragmentos, seleccione el icono _Fragmentos_ ( ![icono Fragmentos](../assets/do-not-localize/icon-fragments.svg) ).

   Puede hacer lo siguiente:

   * Ordenar el listado.
   * Examine, busque o filtre la lista.
   * Cambiar entre las vistas de miniaturas y de lista.
   * Actualice la lista para reflejar cualquiera de los fragmentos creados recientemente.

   ![Seleccionar un fragmento de la lista](assets/visual-designer-fragments.png){width="700" zoomable="yes"}

1. Arrastre y suelte cualquiera de los fragmentos en el componente estructural.

   El editor procesa el fragmento dentro de la sección o el elemento de la estructura de correo electrónico.

   El contenido del fragmento se actualiza dinámicamente dentro de la estructura para previsualizar cómo se procesa el fragmento en el correo electrónico.

<!-- 
>[!BEGINSHADEBOX]

**Editable fields in customizable fragments**

A visual fragment can include editable fields that you can customize. Custom fields allow you to modify parameters when you incorporate the fragment into your content and create a tailored experience without affecting the original fragment. The fragment author can design the fragment for customization of text, image, and button components. If an included fragment contains components with editable fields, you can change the default values to customize it for your content.

1. Select the fragment component.

   The Settings displayed on the right include editable fields with the default values.

   ![Change fragment component parameters](assets/fragment-editable-fields-displayed-design.png){width="700" zoomable="yes"}   

1. Change any editable field as needed.

>[!ENDSHADEBOX]
-->

Una vez guardado el correo electrónico, aparecerá en la página de detalles del fragmento al seleccionar la pestaña _[!UICONTROL Utilizado por]_ en el resumen.

### Añadir recursos de imagen {#insert-image}

Cuando se aprovisiona [!DNL Marketo Optimizer], los recursos existentes de Marketo Design Studio están disponibles en el espacio de diseño de correo electrónico. Puede examinar e insertar estas imágenes en los correos electrónicos directamente desde el selector de recursos.

>[!IMPORTANT]
>
>La disponibilidad de los recursos en [!DNL Marketo Optimizer] se basa en una **copia única** de los recursos de Marketo Design Studio. La modificación de recursos en Marketo Engage después de la copia inicial es **no** reflejada en [!DNL Marketo Optimizer]. También puede cargar recursos de imagen directamente desde el espacio de diseño visual o desde la [biblioteca de Assets](./digital-asset-management.md).

Tipos de archivo de imagen admitidos:

* **Totalmente compatible** (visible en el selector, insertable en línea): JPG, PNG, GIF, WebP.
* **Accesible con advertencias**: SVG (con una advertencia de que algunos clientes de correo electrónico no procesan SVG).
* **No compatible con esta versión de Beta:** TIFF, PDF, DOCX, XLSX, PPTX, CSS, JS, HTML, TXT, archivos binarios, PSD, AI, INDD.

En el espacio de diseño del contenido visual, seleccione el icono _Assets_ ( ![Assets icon](../assets/do-not-localize/icon-assets-me.svg) ) en la barra de navegación izquierda. Desde el selector de recursos, puede seleccionar directamente los recursos almacenados en la biblioteca de Assets.

* Añada un nuevo recurso arrastrando y soltando el recurso de imagen en un componente de estructura.

  ![Arrastre un recurso interno al lienzo y ajuste la configuración](./assets/content-design-add-asset.png){width="800" zoomable="yes"}

* Reemplace un recurso de imagen existente seleccionándolo en el lienzo y haciendo clic en **[!UICONTROL Seleccionar recurso]** en las herramientas de origen de imagen.

  ![Seleccione un recurso de la biblioteca de origen](./assets/content-design-select-an-asset.png){width="600" zoomable="yes"}

Para obtener más información sobre el uso de recursos, consulte [_Uso de recursos para la creación de contenido_](./digital-asset-management.md#assets-authoring).

### Desplazamiento por las capas, la configuración y los estilos {#navigation-layers}

Utilice el árbol de navegación para seleccionar componentes y columnas y, a continuación, ajuste su configuración y estilos en el panel derecho. Ver [árbol de navegación](./structure-components.md#navigation-tree).

### Personalización del contenido {#personalize-content}

[!DNL Marketo Optimizer] utiliza la sintaxis de Handlebars para la personalización. Los tokens se sustituyen en el momento del envío con valores de los datos de perfil de cada destinatario. Existen varios lugares en los que puede utilizar la personalización en un correo electrónico:

* **Línea de asunto**: el punto de personalización más común.
* **Preheader**: se establece dentro del lienzo visual; admite tokens de atributos de perfil.
* **Texto del cuerpo del correo electrónico**: nombres y otros atributos de perfil insertados en línea.
* **URL de botón** — anexar parámetros por destinatario.

>[!NOTE]
>
>En esta versión de Beta, solo los atributos de perfil están disponibles en el Editor de Personalization.

_Para agregar personalización :_

1. En el espacio de diseño de correo electrónico (o en la página de propiedades de correo electrónico de la línea de asunto), haga clic en el campo donde desee insertar un token.
1. Haga clic en el icono _Personalizar_ ( ![Icono Personalizar](../assets/do-not-localize/icon-personalize.svg) ) para usar un token de personalización.
1. En el cuadro de diálogo de personalización, examine el árbol de esquema de la izquierda. Se muestran los atributos de perfil (nombre, apellidos, correo electrónico, cargo y otros campos de perfil).
1. Seleccione un atributo. El editor inserta la expresión Handlebars correspondiente; por ejemplo, `{{profile.firstName}}`.
1. Agregue un valor de reserva para controlar los datos que faltan: `{{profile.firstName | default: "there"}}`.
1. Haga clic en **[!UICONTROL Confirmar]** o **[!UICONTROL Insertar]**. La expresión aparece en línea en el campo.

+++Patrones de personalización comunes {#personalization-patterns}

Use expresiones Handlebars como las siguientes (la personalización usa la misma sintaxis descrita en [Personalizar contenido](#personalize-content)):

* `{{profile.lastName}}` — inserta el apellido del destinatario.
* `{{profile.jobTitle}}` — Hacer referencia al cargo del destinatario en la copia de cuerpo.
* `{{profile.firstName}}, ready to take the next step?` — Combina token y texto estático en línea.

Para un saludo de nombre con una alternativa cuando falte el valor, use el asistente `default` como se muestra en los pasos de personalización anteriores (por ejemplo, nombre con el valor predeterminado `"there"`).

+++

+++Ayudantes de Handlebars {#handlebars-helpers}

Más allá de `default`, el editor de personalización incluye controladores Handlebars integrados para la lógica condicional, la transformación de texto y el formato de fecha. Utilice el explorador de funciones del editor para explorar los ayudantes disponibles e insertarlos con la sintaxis correcta.

>[!TIP]
>
>En el espacio de diseño del correo electrónico, escriba `{{` directamente en cualquier campo de texto para almacenar en déclencheur un menú desplegable de autocompletar en línea que enumere los atributos de perfil disponibles, sin necesidad de abrir el cuadro de diálogo de personalización completo para realizar inserciones rápidas.

+++

+++Expresiones asistidas por IA {#ai-personalization}

El compañero del editor de personalización puede generar expresiones Handlebars a partir de una descripción en lenguaje sencillo, explicar lo que hace una expresión existente e identificar posibles problemas. Utilícelo para acelerar la creación de expresiones, especialmente para la lógica condicional o los ayudantes de formato de fecha.

+++

Para obtener más información acerca de las herramientas y la sintaxis del editor de expresiones, consulte [expresiones Personalization](./personalization-expressions.md).

### Editar seguimiento de URL vinculadas {#preview-and-edit-linked-urls}

{{$include /help/_includes/content-design-links.md}}

## Compruebe y pruebe el correo electrónico {#check-and-test-the-email}

Utilice los controles de escritorio y vista previa para móviles de la barra de herramientas del espacio de diseño de correo electrónico para revisar el diseño del correo electrónico antes de guardarlo. Cambie a la vista previa en modo oscuro para validar la legibilidad y el contraste (consulte [Modo oscuro para el contenido de correo electrónico](./email-dark-mode.md)).

Los perfiles de prueba [!UICONTROL Simular contenido] y enviar flujos de trabajo de revisión no están disponibles en esta versión de Beta. Ver [Limitaciones actuales](../marketing/email-channel.md#limitations) en la descripción general del canal de correo electrónico.

Revise [Validando contenido de correo electrónico](#validation) para las alertas de contenido que debe resolver antes de la activación del recorrido.

## Validación del contenido de correo electrónico {#validation}

Antes de activar el recorrido, el contenido del correo electrónico debe ser válido. [!DNL Marketo Optimizer] muestra alertas de nivel de contenido en el correo electrónico y en el lienzo del recorrido. Esta sección trata sobre las alertas que puede ver y cómo resolverlas.

### Alertas de contenido comunes {#content-alerts}

| Alerta | Lo que significa | Cómo resolver |
| ----- | ------------- | -------------- |
| **Falta la línea de asunto** | El campo Subject line está vacío. | Abra el correo electrónico e introduzca una línea de asunto en la ficha **[!UICONTROL Contenido]**. Se permiten tokens de Personalization, pero el campo no puede estar vacío. |
| **El cuerpo del correo electrónico está vacío** | El lienzo del espacio de diseño del correo electrónico no tiene contenido. | Haga clic en **[!UICONTROL Editar cuerpo del correo electrónico]** para abrir el espacio de diseño del correo electrónico. Arrastre al menos un componente Estructura y un componente Contenido al lienzo y haga clic en Guardar. |
| **Configuración de canal no seleccionada** | No se ha elegido ninguna configuración de canal de correo electrónico para el nodo de correo electrónico. | En la ficha **[!UICONTROL Acciones]**, seleccione una **[!UICONTROL configuración de canal de correo electrónico]** activa. |
| **Configuración de canal eliminada** | La configuración de canal seleccionada anteriormente se ha eliminado o ya no está activa. | En la ficha **[!UICONTROL Acciones]**, seleccione otra **[!UICONTROL configuración del canal de correo electrónico]** activa. Si no hay ninguno disponible, un administrador debe crear o reactivar uno en [Configuración del canal de correo electrónico](../admin/email-channel-configuration.md). |
| **El tamaño del correo electrónico supera los 100 KB** | El tamaño total del correo electrónico (HTML, CSS en línea, contenido codificado) es mayor que el límite de las prácticas recomendadas del ISP de 100 KB. | Reduzca el tamaño del correo electrónico: reemplace las imágenes en línea grandes con imágenes alojadas externamente de Marketo Design Studio, elimine los CSS en línea no utilizados y simplifique las estructuras anidadas. |
| **Token de personalización sin resolver** | Un token de Handlebars hace referencia a un atributo de perfil sin reserva y es posible que falte el atributo para algunos destinatarios. | Agregue una reserva utilizando el asistente de Handlebars `default` como se describe en [Personalizar contenido](#personalize-content). Como alternativa, restrinja la audiencia de recorrido a perfiles en los que el atributo esté garantizado. |
| **Imagen no cargada** | Un componente de imagen hace referencia a un recurso que ya no está disponible. | Haga clic en la imagen, abra el selector de recursos y vuelva a seleccionar el recurso de la biblioteca de Assets. |
