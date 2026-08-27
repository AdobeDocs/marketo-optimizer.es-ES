---
title: Formularios
description: 'Cree y administre formularios reutilizables para la recopilación de datos empresariales: campos de diseño, establezca páginas de agradecimiento, publique y realice un seguimiento del uso en Marketo Optimizer.'
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: 2434
ht-degree: 2%

---

# Formularios

Para capturar información de los visitantes de una página web, cree formularios y agréguelos a las páginas de aterrizaje. Un formulario es un conjunto de campos que los visitantes de la página completan y envían para obtener algún tipo de contenido u oferta, como un documento técnico, un seminario web bajo demanda o una prueba gratuita.

La cantidad de información que debe capturar el formulario depende del valor del contenido o la oferta. Si ofrece algo sencillo, como un documento técnico, recopile solo información mínima, como el nombre, el correo electrónico y la compañía. Si la oferta tiene un valor mayor, como una demostración o una prueba gratuita, puede recopilar más información. El requisito de solicitar un formulario enviado para permitir la visualización de contenido se denomina _contenido cerrado_. Su organización decide qué contenido debe actualizarse y cuál no (_gratis_). La práctica recomendada es permitir cierto contenido de forma gratuita y bloquear solo el contenido premium o de alta demanda.

>[!PREREQUISITES]
>
>Para que los equipos de marketing puedan crear y utilizar formularios para capturar información, un administrador debe definir uno o varios ajustes preestablecidos de formulario. Para obtener más información, consulte [_configuraciones de Forms_](../admin/configuration-presets-forms.md).

<!-- 
>Form creation in [!DNL Marketo Optimizer] requires the following [permissions](../start/user-management.md#b2b-product-permissions):
>
>* _[!UICONTROL Journey Optimizer Library]_ > _[!UICONTROL Read B2C Forms]_ - Required to access and view forms.
>* _[!UICONTROL Journey Optimizer Library]_ > _[!UICONTROL Manage B2C Forms]_ - Required to create, update, and delete forms.
>* _[!UICONTROL Journey Optimizer Library]_ > _[!UICONTROL Publish B2C Forms]_ - Required to publish forms.
-->

## Acceso y administración de formularios {#view-forms}

Para acceder a los formularios de [!DNL Marketo Optimizer], ve a la barra de navegación izquierda y haz clic en **[!UICONTROL Administración de contenido]** > **[!UICONTROL Forms]**. Esta acción abre una página de lista que muestra todos los formularios creados en la instancia.

![Acceder a la biblioteca de formularios](./assets/forms-list.png){width="800" zoomable="yes"}

El sistema ordena la tabla por la columna _[!UICONTROL Modificado]_, y muestra los formularios actualizados más recientemente en la parte superior de forma predeterminada. Haga clic en el título de la columna para cambiar entre ascendente y descendente.

### Estado del formulario y ciclo vital {#form-status}

El estado del formulario determina su disponibilidad para utilizarlo en una página de aterrizaje o plantilla de página de aterrizaje, y los cambios que puede realizar en él.

| Estado | Descripción |
| -------------------- | ----------- |
| Borrador | Al crear un formulario, se encuentra en estado de borrador. Permanece en este estado a medida que define o edita los campos hasta que lo publica para utilizarlo en una página de aterrizaje o plantilla de página de aterrizaje. Acciones disponibles:<br/><ul><li>Editar todos los detalles<li>Editar en el espacio de diseño visual<li>Publicación<li>Duplicado<li>Eliminar |
| Publicadas | Al publicar un formulario, pasa a estar disponible para su uso en una página de aterrizaje o plantilla de página de aterrizaje. El contenido del formulario publicado no se puede modificar en el espacio de diseño visual. Acciones disponibles:<br/><ul><li>Editar nombre, descripción o página de agradecimiento<li>Añadir a una página de aterrizaje o plantilla de página de aterrizaje<li>Crear versión de borrador<li>Duplicado<li>Eliminar (si no está en uso)<li>Código incrustado |
| Publicado con borrador | Cuando crea un borrador a partir de un formulario publicado, la versión publicada permanece disponible para su uso en una página de aterrizaje o plantilla. El contenido del borrador se puede modificar en el espacio de diseño visual. Si publica la versión de borrador, reemplazará la versión publicada actual y el contenido se actualizará en las páginas de aterrizaje o en las plantillas de página de aterrizaje en las que esté en uso. Acciones disponibles:<br/><ul><li>Editar nombre, descripción o páginas de agradecimiento<li>Añadir a una página de aterrizaje o plantilla de página de aterrizaje<li>Editar versión de borrador en el espacio de diseño visual<li>Publicar versión de borrador<li>Duplicado<li>Eliminar (si no está en uso)<li>Código incrustado |

![Ciclo de vida del estado del formulario](assets/status-lifecycle-diagram.png){zoomable="yes"}

### Filtrado de la lista de formularios {#filter-list}

Para buscar un formulario por nombre, introduzca una cadena de texto en la barra de búsqueda para buscar una coincidencia. Haga clic en el icono _Filtro_ ( ![Mostrar u ocultar el icono de filtros](../assets/do-not-localize/icon-filter.svg) ) para mostrar las opciones de filtro disponibles y cambiar la configuración para filtrar los elementos mostrados según los criterios especificados.

![Filtrar los formularios mostrados](assets/forms-list-filtered.png){width="700" zoomable="yes"}

### Personalización de la visualización de columnas {#column-display}

Personalice las columnas que desee mostrar en la tabla haciendo clic en el icono _Personalizar tabla_ ( ![Personalizar icono de tabla](../assets/do-not-localize/icon-column-settings.svg) ) en la parte superior derecha.

En el cuadro de diálogo, seleccione las columnas que desea mostrar y haga clic en **[!UICONTROL Aplicar]**.

![Columnas para mostrar en la lista de Forms](assets/forms-customize-table-dialog.png){width="300"}

## Creación de formularios {#create-forms}

Hay varias cosas que hay que tener en cuenta antes de empezar a crear formularios reutilizables en [!DNL Marketo Optimizer]:

* Determine qué formularios necesita.

  Es posible utilizar solo cuatro formularios estándar. Uno para acceder a contenido descargable, otro para acceder a páginas web premium, otro para ver vídeos y otro para registrarse en cosas como seminarios web. Si alguna vez necesita cambiar un campo en un formulario, es más fácil actualizar cuatro formularios estándar que se utilizan globalmente en lugar de cambiar varios formularios distribuidos en todos los programas de marketing.

  <!-- Global forms also make progressive profiling much easier to implement. -->

* Para cada formulario estándar, determine qué campos utilizar y cómo presentarlos.

  Considere utilizar formularios más cortos, ya que se ha comprobado que son mejores para las conversiones. Cuando revise cada formulario, decida qué campos son razonables y necesarios para su propósito.

  Tenga en cuenta si debe rellenar previamente los campos de formulario para que la información básica, como el nombre y el correo electrónico, esté rellenada previamente. Pero otra información, como el cargo y el tamaño de la organización, no lo es. De este modo, el visitante solo debe rellenar dos campos y enviar el formulario. También puede utilizar un formulario social para rellenarlo con datos de Facebook o Twitter.

* Planifique qué página de seguimiento se mostrará después de que un visitante envíe un formulario (página _gracias_).

  ¿Todos obtienen la misma página o es dinámica y se basa en sus datos? Por ejemplo, alguien en la industria de la atención médica podría ver un contenido de página diferente a alguien en la industria tecnológica.

* Considere si desea omitir un formulario por completo si ya tiene la información que necesita.

  Cuando permite que se omita un formulario para una persona conocida que visita la página de aterrizaje, simplemente puede acceder al contenido directamente. Omitir el formulario ofrece una experiencia de visitante más ágil.

### Añadir un nuevo formulario {#new-form}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_form_preset"
>title="Selección de un ajuste preestablecido"
>abstract="Elija un ajuste preestablecido que contenga la conexión que se va a utilizar y un conjunto de datos predefinido para el formulario."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/prime/admin/channels/configuration-presets-forms#create-preset" text="Crear un ajuste preestablecido de un formulario"

Puede crear un formulario en [!DNL Marketo Optimizer] haciendo clic en **[!UICONTROL Crear formulario]** en la parte superior derecha de la página de lista de _[!UICONTROL Forms]_.

1. En el cuadro de diálogo _[!UICONTROL Crear formulario]_, escriba un **[!UICONTROL Nombre]** (obligatorio) y una **[!UICONTROL Descripción]** (opcional) útiles.

   Requisitos de formulario:

   * Nombre: máximo de 100 caracteres, debe ser único, sin distinción de mayúsculas y minúsculas
   * Descripción: máximo de 300 caracteres
   * Se permiten caracteres Alpha, numéricos y especiales
   * Los caracteres reservados **_no se permiten_**: `\ / : * ? " < > |`

   ![Crear cuadro de diálogo de formulario](assets/forms-create-dialog.png){width="400"}

1. Para **[!UICONTROL Ajuste preestablecido]**, haga clic en el icono _Seleccionar datos_ ( ![Icono de selección de datos](../assets/do-not-localize/icon-select-data.svg) ) para vincular un ajuste preestablecido de formulario configurado con el formulario.

   El ajuste preestablecido determina dónde se almacenan y reflejan las respuestas del formulario. Puede introducir una cadena de texto para buscar un ajuste preestablecido específico o seleccionarlo en la lista.

1. Haga clic en **[!UICONTROL Crear]**.

   Se abrirá la página de detalles del formulario con una definición de formulario básica predeterminada.

   ![Contenido de formulario predeterminado](assets/form-new-default-content.png){width="700" zoomable="yes"}

### Cambiar el diseño de formulario predeterminado {#design}

Utilice las herramientas de diseño visual para cambiar el contenido del formulario según sea necesario:

* [Añadir campos](./form-design.md#add-field)
* [Cambiar estilo de campo](./form-design.md#field-styling)
* [Reordenar campos](./form-design.md#field-reorder)
* [Cambiar texto y estilo del botón de envío](./form-design.md#submit-button)
* [Cambio del estilo del formulario](./form-design.md#form-styling)

Haga clic en **[!UICONTROL Guardar y cerrar]** para guardar los cambios de diseño del contenido del formulario y vaya a los detalles del formulario.

### Configurar la página de agradecimiento {#thank-you-page}

En el panel _[!UICONTROL Resumen]_ de la derecha, desplácese hasta la sección **[!UICONTROL Página de agradecimiento]** y use la configuración **[!UICONTROL Realizar seguimiento con]** para definir lo que sucede cuando un visitante envía el formulario:

* **[!UICONTROL Permanecer en la página]**: elija esta opción para mantener al visitante en la misma página cuando se envíe el formulario.
* **[!UICONTROL Página de aterrizaje]**: elija esta opción para seleccionar cualquier página de aterrizaje [!DNL Marketo Optimizer] como seguimiento.
* **[!UICONTROL Dirección URL externa]**: elija esta opción para especificar cualquier dirección URL como página de seguimiento. Una vez que el visitante envía el formulario, el explorador carga la dirección URL designada.

  >[!TIP]
  >
  >Si desea utilizar el formulario para descargar un archivo, puede especificar una dirección URL para el archivo alojado. Con esta configuración, el botón de envío funciona como un botón de descarga.

### Publicar el borrador del formulario {#publish}

Cuando esté listo para que el formulario esté disponible para usarlo en una página de aterrizaje o plantilla de página de aterrizaje, haga clic en **[!UICONTROL Publicar]**.

![Cuadro de diálogo Publicar formulario](assets/form-publish-dialog.png){width="400"}

Esta acción abre un cuadro de diálogo de confirmación. Puede anular el proceso de publicación haciendo clic en **[!UICONTROL Cancelar]** o en **[!UICONTROL Publicar]** para confirmar.

## Ver detalles del formulario {#view-details}

Haga clic en el nombre de cualquier formulario de la página de la lista para abrir la página de detalles del formulario. Puede editar el formulario, cambiarle el nombre o actualizar su descripción. Realice actualizaciones y haga clic fuera del nombre o del campo de descripción para guardar automáticamente los cambios.

>[!NOTE]
>
>Si una página de aterrizaje o plantilla de página de aterrizaje está utilizando un formulario publicado, no puede editar el contenido ni cambiar la página de agradecimiento. Puede crear una versión de borrador si desea realizar cambios en el formulario.

![Ver detalles de un formulario publicado](assets/form-details-published.png){width="600" zoomable="yes"}

Haga clic en **[!UICONTROL Editar formulario]** para abrir el formulario en el espacio de diseño visual.

Salga de la vista en cualquier momento haciendo clic en la flecha _Atrás_ en la parte superior izquierda, que le lleva a la página de lista _[!UICONTROL Forms]_.

## Ver formulario utilizado por referencias {#used-by}

En el panel _[!UICONTROL Resumen]_ de la derecha, haz clic en la pestaña **[!UICONTROL Utilizado por]** para ver los detalles de dónde se usa actualmente el formulario en [!DNL Marketo Optimizer], en las páginas de aterrizaje y en las plantillas de páginas de aterrizaje.

>[!IMPORTANT]
>
>No se puede eliminar ningún formulario que esté en uso actualmente en una página de aterrizaje o plantilla de página de aterrizaje.

![Utilizado por referencias para el formulario](assets/form-used-by-published.png){width="600" zoomable="yes"}

Las referencias se muestran según la categoría: _Página de aterrizaje_ o _Plantilla de página de aterrizaje_. Haga clic en el vínculo para abrir la página o plantilla correspondiente donde se utiliza el formulario.

## Eliminar formularios {#delete-forms}

No se puede eliminar ningún formulario que una página de aterrizaje o plantilla de página de aterrizaje esté utilizando en ese momento. Puede comprobar las referencias _utilizadas por_ antes de iniciar la eliminación de un formulario. Además, una eliminación no se puede deshacer, por lo que debe comprobarla antes de iniciar una acción de eliminación.

Puede eliminar un formulario mediante cualquiera de los siguientes métodos:

* En la parte superior derecha, haga clic en **[!UICONTROL ... Más]** y elige **[!UICONTROL Eliminar]**.
* En la página de lista _[!UICONTROL Forms]_, haga clic en _Más_ (**...**) junto al nombre del formulario y elija **[!UICONTROL Eliminar]**.

Esta acción abre un cuadro de diálogo de confirmación. Puede anular el proceso haciendo clic en **[!UICONTROL Cancelar]** o en **[!UICONTROL Eliminar]** para confirmar la eliminación.

![Cuadro de diálogo Eliminar formulario](assets/form-delete-dialog.png){width="400"}

Si el formulario está en uso, la acción abre un cuadro de diálogo informativo que le avisa de que no se puede eliminar. Haga clic en **[!UICONTROL Aceptar]**, lo que anula la acción de eliminación.

![Cuadro de diálogo Eliminar formulario: no se puede eliminar el formulario en uso](assets/form-delete-dialog-in-use.png){width="400"}

## Formularios duplicados {#duplicate-forms}

Duplicar un formulario es una forma rápida y sencilla de crear un nuevo formulario utilizando un formulario existente como punto de partida para el diseño de formularios.

Puede duplicar un formulario mediante cualquiera de los siguientes métodos:

* En la parte superior derecha de la página de detalles del formulario, haga clic en **[!UICONTROL ... Más]** y elige **[!UICONTROL Duplicar]**.
* En la página de lista _[!UICONTROL Forms]_, haga clic en _Más_ (**...**) junto al nombre del formulario y elija **[!UICONTROL Duplicar]**.

![Duplicar el formulario](assets/form-list-page-duplicate.png){width="450"}

En el cuadro de diálogo, introduzca un nombre útil (único) y una descripción. Haga clic en **[!UICONTROL Duplicar]** para completar la acción.

![Nombre y descripción para el formulario duplicado](assets/form-duplicate-dialog.png){width="400"}

Edite el formulario duplicado para cambiar el nombre según sea necesario y modificar el formulario para el uso previsto.

## Editar formularios {#edit-forms}

Los cambios realizados en un formulario dependen de su estado actual:

* Cuando un formulario está en estado _Borrador_, puede editar cualquiera de sus detalles y contenido (campos, botón y estilo).
* Cuando un formulario se encuentra en estado _Publicado_, puede editar el nombre o la descripción del formulario. No puede editar el contenido.
* Cuando un formulario se encuentra en _Publicado con el estado Borrador_, puede editar el nombre o la descripción del formulario. En la versión de borrador, también puede editar el contenido y la página de agradecimiento.

>[!BEGINTABS]

>[!TAB Borrador]

1. En la página de lista _[!UICONTROL Forms]_, haga clic en el nombre del formulario para abrirlo.

   Se muestra una vista previa del contenido del formulario, con los detalles del formulario a la derecha.

1. Modifique cualquiera de los detalles, como el nombre y la descripción.

   ![Detalles del formulario con estado Borrador](assets/form-details-draft.png){width="600" zoomable="yes"}

1. Para realizar cambios en el formulario en el espacio de diseño visual, haga clic en **[!UICONTROL Editar formulario]**.

   Utilice las herramientas de diseño visual según sea necesario:

   * [Añadir campos](./form-design.md#add-field)
   * [Cambiar estilo de campo](./form-design.md#field-styling)
   * [Reordenar campos](./form-design.md#field-reorder)
   * [Cambiar texto y estilo del botón de envío](./form-design.md#submit-button)
   * [Cambio del estilo del formulario](./form-design.md#form-styling)

   Haga clic en **[!UICONTROL Guardar y cerrar]** para volver a los detalles del formulario.

1. Cuando el formulario cumpla sus criterios y desee que esté disponible para usarlo en una página de aterrizaje o plantilla de página de aterrizaje, haga clic en **[!UICONTROL Publicar]**.

>[!TAB Publicado]

1. En la página de lista _[!UICONTROL Forms]_, haga clic en el nombre del formulario para abrirlo.

   Se muestra una vista previa del contenido del formulario, con los detalles del formulario a la derecha.

1. Para crear una versión de borrador para editar el formulario, haga clic en **[!UICONTROL Editar formulario]** en el panel _[!UICONTROL Resumen]_ de la derecha.

1. Haga clic en **[!UICONTROL Crear versión de borrador]** en el cuadro de diálogo para abrir la versión de borrador en el espacio de diseño visual.

   ![Cuadro de diálogo Crear versión de borrador](assets/form-published-edit-create-draft-dialog.png){width="400"}

1. Utilice las herramientas de diseño visual que sean necesarias para actualizar el contenido del formulario:

   * [Añadir campos](./form-design.md#add-field)
   * [Cambiar estilo de campo](./form-design.md#field-styling)
   * [Reordenar campos](./form-design.md#field-reorder)
   * [Cambiar texto y estilo del botón de envío](./form-design.md#submit-button)
   * [Cambio del estilo del formulario](./form-design.md#form-styling)

   Haga clic en **[!UICONTROL Guardar y cerrar]** para volver a los detalles del formulario.

1. Cuando el borrador del formulario cumpla con sus criterios y desee que los cambios estén disponibles para usarlos en una página de aterrizaje o plantilla de página de aterrizaje, haga clic en **[!UICONTROL Publicar]**.

   Cuando publica la versión de borrador, reemplaza la versión publicada actual y el contenido del formulario se actualiza en las páginas de aterrizaje o en las plantillas de página de aterrizaje donde ya se utiliza.

>[!TAB Publicado con borrador]

1. Haga clic en el nombre del formulario para abrirlo.
1. Seleccione la ficha **[!UICONTROL Borrador]**.

   Se muestra una vista previa del contenido del formulario de la versión del borrador, con los detalles del formulario a la derecha.

   ![Editar la versión de borrador del formulario](assets/form-published-with-draft-edit.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Editar formulario]** en el panel _[!UICONTROL Resumen]_ de la derecha y use las herramientas de diseño visual según sea necesario:

   * [Añadir campos](./form-design.md#add-field)
   * [Cambiar estilo de campo](./form-design.md#field-styling)
   * [Reordenar campos](./form-design.md#field-reorder)
   * [Cambiar texto y estilo del botón de envío](./form-design.md#submit-button)
   * [Cambio del estilo del formulario](./form-design.md#form-styling)

   Haga clic en **[!UICONTROL Guardar y cerrar]** para volver a los detalles del formulario.

1. Cuando el borrador del formulario cumpla con sus criterios y desee que los cambios estén disponibles para usarlos en páginas de aterrizaje y plantillas de páginas de aterrizaje, haga clic en **[!UICONTROL Publicar]**.

   Cuando publique la versión de borrador, reemplazará la versión publicada actual y el formulario se actualizará en las páginas de aterrizaje y plantillas donde ya esté en uso.

>[!ENDTABS]

## Agregar formularios a una página de aterrizaje o plantilla {#insert-forms}

Los Forms están diseñados para ser reutilizados y se pueden insertar al diseñar una [página de aterrizaje](./landing-pages.md).

<!-- or [landing page template](./landing-page-templates.md). -->

{{$include /help/_includes/content-design-add-forms.md}}

## Acciones de formulario para la creación de páginas y plantillas {#form-actions}

Cuando se incluye un formulario en una página de aterrizaje o plantilla de página de aterrizaje, el contenido del formulario no se puede cambiar dentro de la página o plantilla. Sin embargo, puede aplicar las siguientes acciones:

* **[!UICONTROL Eliminar]**: esta acción quita el formulario del contenido de la página o plantilla actual (el origen del formulario no se ve afectado).
* **[!UICONTROL Duplicado]**: esta acción duplica el formulario en el editor y mantiene las mismas dimensiones.
* **[!UICONTROL Ver HTML]**: esta acción abre una ventana emergente con la HTML para el formulario. Puede editar HTML o copiarlo para utilizarlo en otro contenido web.
* **[!UICONTROL Editar formulario]**: esta acción abre una nueva pestaña del explorador con la página del editor de formularios y los detalles.

Al seleccionar el formulario en el espacio de diseño de la página de aterrizaje, estas acciones están disponibles en la barra de herramientas de contexto y en el panel de propiedades de la derecha.

![Aplicar acciones al formulario seleccionado](assets/form-actions-page-authoring.png){width="600" zoomable="yes"}
