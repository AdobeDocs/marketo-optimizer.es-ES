---
title: Crear y publicar de páginas de aterrizaje
description: 'Cree, diseñe y publique páginas de aterrizaje para recorridos de personas: genere desde cero, importe HTML, añada formularios, personalice contenido y vincule desde correos electrónicos en Marketo Optimizer.'
feature: Landing Pages, Content Design Tools
role: User
TQID: 'https://experienceleague.adobe.com/XIXt4QcgK7VALQqpPHf6GqhCwEsV3mlyV1ZrgrIXi0s'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 3cf5f37e-e87e-5179-812b-53ce05d7eebbid: 64b90904-e4f0-5c1b-a871-8c6a40b204a1id: 8881ff95-1653-5fea-82af-ce1549c0d99d
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 1550
ht-degree: 11%

---

# Creación y publicación de páginas de destino

Como especialista en marketing, puede definir y publicar páginas que desee incorporar en los recorridos. Cuando se agrega una nueva página de aterrizaje, se configura la página principal y las subpáginas, se diseña el contenido, se prueba y se publica.

![Diagrama del flujo de trabajo de la página de aterrizaje](assets/landing-page-work-flow-diagram-no-subpages.svg)

>[!BEGINSHADEBOX]

## Requisitos previos de página de aterrizaje {#landing-page-prerequisites}

Para que los especialistas en marketing puedan crear páginas de aterrizaje que admitan sus recorridos, deben haberse configurado las siguientes configuraciones y recursos:

* [Subdominio de página de aterrizaje](../admin/configuration-presets-landing-pages.md#lp-subdomains): configure un subdominio dedicado a alojar sus páginas de aterrizaje.
* [Ajuste preestablecido de página de aterrizaje](../admin/configuration-presets-landing-pages.md#lp-presets): un ajuste preestablecido define el subdominio y otra configuración aplicada a sus páginas de aterrizaje.
* [Formulario](./forms.md) (para casos de uso de captura de datos): requerido cuando desee incrustar un formulario en una página de aterrizaje y enviar datos a Experience Platform.

>[!ENDSHADEBOX]

## Creación de una página de destino {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_create"
>title="Definir y configurar la página de destino"
>abstract="Para crear una página de destino, debe seleccionar un ajuste preestablecido, configurar la página principal y las subpáginas y, por último, probar la página antes de publicarla."

Para dirigir a los miembros de una audiencia de recorrido a una página web definida cuando hagan clic en un vínculo específico, cree una página de aterrizaje en [!DNL Marketo Optimizer].

>[!IMPORTANT]
>
>Antes de crear la primera página de aterrizaje, complete la configuración de esta. Esto incluye configurar un subdominio para alojar las páginas de aterrizaje y definir al menos un ajuste preestablecido que especifique el subdominio y otras opciones de configuración de canal. Puede seleccionar un ajuste preestablecido al crear la página de aterrizaje. Para obtener información de configuración del administrador, consulte [Configuración de la página de aterrizaje](../admin/configuration-presets-landing-pages.md).
>
>En los casos de uso de captura de datos, cree un [formulario](./forms.md) antes de incrustarlo en una página de aterrizaje.

_Para crear una página de aterrizaje :_

1. Vaya a la navegación de la izquierda y seleccione **[!UICONTROL Administración de contenido]** > **[!UICONTROL Páginas de aterrizaje]**.

1. En la lista de páginas de aterrizaje, haga clic en **[!UICONTROL Crear página de aterrizaje]**.

1. Escriba **[!UICONTROL Título]** (obligatorio) y **[!UICONTROL Descripción]** (opcional).

   Título y criterios de descripción:

   * **Título**: máximo de 100 caracteres. Debe ser único (sin distinción de mayúsculas y minúsculas).
   * **Descripción**: máximo de 300 caracteres.
   * Se permiten caracteres Alpha, numéricos y especiales.
   * Los caracteres reservados **_no se permiten_**: `\ / : * ? " < > |`

   ![Crear página de aterrizaje](assets/landing-page-create.png){width="600"}

1. Seleccione un **[!UICONTROL ajuste preestablecido]**.

   Un administrador [crea ajustes preestablecidos de página de aterrizaje](../admin/configuration-presets-landing-pages.md#lp-presets) para definir el subdominio y otras opciones de configuración utilizadas para las páginas de aterrizaje. Seleccione un ajuste preestablecido y haga clic en **[!UICONTROL Ver ajuste preestablecido]** para revisar su configuración y confirmar que coincida con los requisitos de la página de aterrizaje.

1. Haga clic en **[!UICONTROL Crear]**.

   Se muestran la página principal y sus propiedades. Aprenda a [configurar la página principal](#configure-primary-page).

   ![Nueva página de aterrizaje - propiedades de la página principal](assets/landing-page-primary-new-properties.png){width="700" zoomable="yes"}

1. Para agregar una subpágina (por ejemplo, una página de agradecimiento o de error), haga clic en el icono **+**.

   Puede agregar hasta dos subpáginas por página de aterrizaje.

Después de configurar y diseñar la página principal y las subpáginas, [pruebe la página de aterrizaje](#test-landing-page) antes de publicarla.

>[!CAUTION]
>
>No puede acceder a la página de aterrizaje copiando y pegando la dirección URL definida en un explorador web, aunque la página esté publicada. Pruebe la página con la función de vista previa como se describe en [Pruebe la página de aterrizaje](#test-landing-page).

## Configuración de la página principal {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_primary_page"
>title="Definir la configuración de la página principal"
>abstract="Defina la página principal, que se muestra inmediatamente cuando un destinatario hace clic en el vínculo de la página de aterrizaje, como desde un correo electrónico o un sitio web."

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_access_settings"
>title="Definir la dirección URL de la página de destino"
>abstract="En esta sección, defina una dirección URL de página de destino única. La primera parte de la dirección URL requiere que haya configurado previamente un subdominio de página de destino como parte del ajuste preestablecido que ha seleccionado."

La página principal es la página que se muestra inmediatamente cuando un destinatario hace clic en el vínculo de la página de aterrizaje, como desde un correo electrónico o un sitio web.

_Para definir la configuración de la página principal :_

1. Cambie **[!UICONTROL Page Name]** según sus necesidades, que es _Primary page_ de forma predeterminada.

1. Defina la parte final de la dirección URL de la página.

   El ajuste preestablecido que ha seleccionado determina la primera parte de la dirección URL. Un administrador configura el [subdominio de página de aterrizaje](../admin/configuration-presets-landing-pages.md#lp-subdomains) como parte del ajuste preestablecido.

   >[!CAUTION]
   >
   >La dirección URL de la página de aterrizaje debe ser única.
   >
   >No puede acceder a la página de aterrizaje copiando y pegando esta URL en un explorador web, aunque la página esté publicada. Pruébelo utilizando la función de vista previa como se describe en [Pruebe la página de aterrizaje](#test-landing-page).

1. Si desea una página de aterrizaje anónima, deshabilite la opción **[!UICONTROL Requerir usuarios identificados]**.

1. Haga clic en el icono _Calendario_ ( ![Icono de calendario](../assets/do-not-localize/icon-calendar.svg) ) para establecer la **[!UICONTROL caducidad de la página]**.

   Después de seleccionar una fecha de caducidad, elija la acción tras la caducidad de la página:

   * **[!UICONTROL URL de redireccionamiento]**: introduzca la URL de la página que se utilizará como redireccionamiento.

     ![Caducidad de la página de aterrizaje: URL de redireccionamiento](assets/landing-page-expiry-redirect-url.png){width="400"}

   * **[!UICONTROL Error del explorador]**: escriba el texto del error que se mostrará en lugar de la página.

     ![Caducidad de la página de aterrizaje: error del explorador](assets/landing-page-expiry-browser-error.png){width="400"}

## Elija el tipo de diseño de contenido {#choose-design-type}

Para agregar _[!UICONTROL Contenido]_ para la página, haga clic en **[!UICONTROL Abrir Designer]**. El proceso de diseño comienza con la elección de cómo desea comenzar:

* [Diseñe desde cero](#design-from-scratch)
* [Importar HTML](#import-html)

![Elige cómo deseas iniciar el diseño de tu página de aterrizaje](assets/landing-page-create-design.png){width="800" zoomable="yes"}

Después de seleccionar el método preferido para iniciar el diseño de la página de aterrizaje, usa las herramientas de diseño visual para [completar el contenido de la página](./landing-page-design.md).

### Diseñe desde cero {#design-from-scratch}

Utilice el espacio de diseño de contenido visual para definir la estructura y el contenido de la página de aterrizaje. Al añadir y mover componentes estructurales con sencillas acciones de arrastrar y soltar, puede diseñar el diseño y la organización del contenido de la página en cuestión de segundos.

1. En la página de inicio de diseño, seleccione la opción **[!UICONTROL Diseñar desde cero]**.

1. [Agregar estructura y contenido](./landing-page-design.md#structure-content-landing-page) a la página.

1. [Revisar y editar el seguimiento de direcciones URL vinculadas](./landing-page-design.md#linked-url-tracking).

1. [Probar la página de aterrizaje](#test-landing-page).

Cuando esté satisfecho con el contenido, haga clic en **[!UICONTROL Guardar]**.

### Importar HTML {#import-html}

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

![Importar contenido de HTML en un archivo zip](assets/templates-import-zip-file.png){width="500"}

>[!NOTE]
>
>El uso de una etiqueta `<table>` como primera capa de un archivo HTML puede causar la pérdida de estilo, incluida la configuración del fondo y el ancho en la etiqueta de la capa superior.

Puede personalizar el contenido importado según sea necesario con las herramientas de diseño visuales.

## Comprobación de alertas {#check-alerts}

Al diseñar el contenido de la página de aterrizaje, las alertas aparecen en la parte superior derecha cuando falta la configuración clave.

![Alertas por problemas con el contenido de la página](assets/alerts-button.png){width="250"}

Si no ve este botón, no se detectan problemas.

Existen dos tipos de alertas:

* **_Advertencias_** que hacen referencia a recomendaciones y prácticas recomendadas, como:

  * `Placeholder links are present in the landing page body`: no olvide reemplazar los marcadores de posición con vínculos válidos.

  * `Text version of HTML is empty`: no se olvide de definir una versión de texto del cuerpo de la página, que se utilizará cuando no se pueda mostrar el contenido de HTML.

  * `Empty link is present in page body`: compruebe que todos los vínculos de la página sean correctos.

* **_Errores_** que impiden probar o activar la recorrido mientras no se resuelvan, como:

  * `The landing page content is empty`: el contenido de la página es obligatorio.

## Prueba de la página de destino {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_preview_lp_profiles"
>title="Previsualizar y probar la página de destino"
>abstract="Tras definir la configuración y el contenido de la página de destino, utilice perfiles de prueba para previsualizar la página."

Cuando se definen la configuración y el contenido de la página de aterrizaje, puede utilizar perfiles de prueba para previsualizar la página. Si ha insertado [contenido personalizado](./landing-page-design.md#personalize-content), puede comprobar cómo se muestra este contenido en la página de aterrizaje mediante los datos del perfil de prueba.

>[!PREREQUISITES]
>
>Para obtener una vista previa y probar páginas de aterrizaje, debe tener el permiso **[!UICONTROL Publicar mensajes]** y un conjunto de datos definido que contenga perfiles de prueba.

1. Haga clic en **[!UICONTROL Previsualizar y probar]** para abrir la selección del perfil de prueba.

   >[!NOTE]
   >
   >También puede usar **[!UICONTROL Simular contenido]** cuando se encuentre en el espacio de diseño visual.

1. En la pantalla _[!UICONTROL Simular]_, seleccione un perfil de prueba.

   ![Simular contenido de página de aterrizaje para el perfil seleccionado](assets/landing-page-simulate.png){width="700" zoomable="yes"}

   Si los perfiles que necesita no aparecen en la lista, haga clic en **[!UICONTROL Administrar perfiles de prueba]** para usar una dirección de correo electrónico de perfil de prueba conocida y agregarla a la lista.

   +++Añadir perfiles de prueba

   Para el área de nombres de identidad **[!UICONTROL Identity]**, haga clic en el icono _Seleccionar_ ( ![Seleccionar icono](../assets/do-not-localize/icon-select-data.svg) ) y elija el área de nombres `Email` que se utilizará para probar los perfiles.

   ![Administrar conjunto de perfiles de prueba Área de nombres de identidad de correo electrónico](assets/manage-test-profiles.png){width="700" zoomable="yes"}

   En el campo **[!UICONTROL Valor de identidad]**, escriba la dirección de correo electrónico para identificar el perfil de prueba y haga clic en **[!UICONTROL Agregar perfil]**. Puede repetir esto para agregar varios perfiles.

   ![Administrar perfiles de prueba y agregar perfiles](assets/manage-test-profiles-add.png){width="700" zoomable="yes"}

   Haga clic en la flecha hacia atrás en la parte superior izquierda para regresar a la página _[!UICONTROL Simular]_.

   +++

1. Seleccione **[!UICONTROL Abrir vista previa]** para probar la página de aterrizaje.

   La vista previa de la página de aterrizaje se abre en una nueva pestaña. Los datos del perfil de prueba seleccionados reemplazan a los elementos personalizados.

   ![Vista previa de la página de aterrizaje con datos de perfil](assets/landing-page-preview.png){width="600"}

1. Seleccione otros perfiles de prueba para previsualizar el procesamiento de cada variante de la página de aterrizaje.

## Publicación de la página {#publish-landing-page}

>[!PREREQUISITES]
>
>Para publicar páginas de aterrizaje, debe tener el permiso **[!UICONTROL Publicar mensajes]**. Antes de publicar, [compruebe y resuelva todas las alertas](#check-alerts).

Cuando la página de borrador cumpla tus criterios y quieras que esté disponible para vincularla en tus mensajes de recorrido, haz clic en **[!UICONTROL Publicar]** en la parte superior derecha. En el cuadro de diálogo de confirmación, haga clic de nuevo en **[!UICONTROL Publicar]** para confirmar.

![Cuadro de diálogo de confirmación para publicar](assets/landing-page-publish-confirm.png){width="250"}

Cuando se publica la página de aterrizaje, se muestra en la lista de la página de aterrizaje con el estado **_[!UICONTROL Publicado]_**. Esto significa que está activo y listo para utilizarse en un mensaje de correo electrónico o SMS enviado a través de un recorrido.

No puede acceder a la página de aterrizaje publicada copiando y pegando la URL en un explorador web. Puede probarlo en cualquier momento con la [función de vista previa](#test-landing-page).
