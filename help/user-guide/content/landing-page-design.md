---
title: Diseño de página de aterrizaje
description: 'Diseñe páginas de aterrizaje con herramientas visuales: añada componentes de contenido, formularios, CSS personalizado, personalización y previsualización de dispositivos para recorridos de persona en Marketo Optimizer.'
feature: Landing Pages, Content Design Tools
role: User
TQID: 'https://experienceleague.adobe.com/zb7rXCj7iWnk8Src1sWLZaYgRa35GjqGxXXu0pTJ-ds'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 556
ht-degree: 2%

---

# Diseño de la página de destino

Después de [crear una página de aterrizaje](./landing-pages-create-publish.md#create-landing-page), use el espacio de diseño visual para crear los componentes estructurales y de contenido en su página.

## Añadir estructura y contenido {#structure-content-landing-page}

{{$include /help/_includes/content-design-components-prime.md}}

### Añadir CSS personalizado {#add-custom-css}

Puede agregar su propio CSS personalizado directamente en el espacio de diseño de la página de aterrizaje. Utilice CSS personalizado para aplicar un estilo avanzado y específico, para una mayor flexibilidad y control sobre el aspecto del contenido. Se recomienda añadir este estilo de nivel superior antes de incluir componentes como imágenes, botones y texto.

Con al menos un componente de contenido en el lienzo, selecciona el componente **[!UICONTROL Cuerpo]** en el árbol de navegación izquierdo para acceder al editor CSS personalizado.

![Acceder a los estilos del cuerpo](assets/landing-page-body-styles-css.png){width="800" zoomable="yes"}

Consulte [Agregar CSS personalizado para el contenido](./design-custom-css.md) para ver los pasos, las reglas de sintaxis y la solución de problemas.

### Añadir recursos {#add-assets}

En el espacio de diseño visual, seleccione el icono _Assets_ ( ![Assets icon](../assets/do-not-localize/icon-assets-me.svg) ) en la barra de navegación izquierda para examinar y seleccionar recursos de imagen de la biblioteca de recursos [!DNL Marketo Optimizer].

Para ver los pasos para seleccionar, reemplazar o cargar recursos de imagen, consulte [Usar recursos para la creación de contenido](./digital-asset-management.md#assets-authoring).

### Añadir formularios {#add-forms}

{{$include /help/_includes/content-design-add-forms.md}}

### Desplazamiento por las capas, la configuración y los estilos {#navigate-layers-settings-styles}

{{$include /help/_includes/content-design-navigation.md}}

### Personalización del contenido {#personalize-content}

[!DNL Marketo Optimizer] utiliza la sintaxis de Handlebars para la personalización. Los tokens se sustituyen por valores de los datos de perfil de cada visitante cuando se visualiza la página de aterrizaje.

_Para agregar personalización :_

1. Seleccione el componente de texto y haga clic en el icono _Agregar personalización_ ( ![Icono de personalización](../assets/do-not-localize/icon-personalize.svg) ) de la barra de herramientas.
1. En el cuadro de diálogo de personalización, examine el árbol de esquema de la izquierda y seleccione un atributo. El editor inserta la expresión Handlebars correspondiente.
1. Agregue un valor de reserva para gestionar los datos que faltan, si es necesario.
1. Haga clic en **[!UICONTROL Confirmar]** o **[!UICONTROL Insertar]**. La expresión aparece en línea en el campo.

Para obtener más información sobre las herramientas y la sintaxis del editor de expresiones, consulte [Editor de Personalization](./personalization-expressions.md).

### Editar seguimiento de URL vinculadas {#linked-url-tracking}

{{$include /help/_includes/content-design-links.md}}

![Haga clic en el icono Editar para acceder al seguimiento de vínculos](assets/landing-page-link-tracking.png){width="400"}

Use **[!UICONTROL Tipo de seguimiento]** para controlar el seguimiento del vínculo:

* **[!UICONTROL Rastreado]**: activa el seguimiento en la dirección URL del vínculo.
* **[!UICONTROL Nunca]**: Nunca activa el seguimiento de la dirección URL del vínculo.

### Guarde el trabajo {#save-your-work}

Haga clic en **[!UICONTROL Guardar]** en cualquier momento para guardar el borrador de la página de aterrizaje.

Puede seguir editando en la página de borrador. Cuando esté listo para mostrar la página y permitir su vinculación en un mensaje de correo electrónico o SMS, puede publicar la página.

### Ver opciones {#view-options}

Aproveche las opciones de vista y validación de contenido disponibles en el espacio de diseño visual.

* Acercar/alejar el contenido en las opciones de zoom preestablecidas.

* Cambie la visualización del contenido en Escritorio, Móvil o Solo texto/Texto sin formato.
  * Haz clic en el icono _Ver_ para obtener una vista previa del contenido entre dispositivos.
  * Seleccione uno de los dispositivos predeterminados o introduzca dimensiones personalizadas para obtener una vista previa del contenido.

### Más opciones {#more-options}

En el menú _[!UICONTROL Más...]_ de la parte superior del espacio de diseño visual, puede realizar las siguientes acciones:

![Haga clic en más para acceder a las acciones de la página de aterrizaje](assets/landing-page-designer-more-menu.png){width="500"}

* **[!UICONTROL Restablecer página de aterrizaje]**: haga clic en esta opción para borrar el lienzo de diseño visual de una pizarra en blanco y reiniciar la creación del contenido de la página.
* **[!UICONTROL Cambia tu diseño]** - Vuelve a la página de inicio de _[!UICONTROL Crear tu página de aterrizaje principal]_. Desde allí, puede elegir otra plantilla para reiniciar el proceso de diseño o elegir diseñar la página desde cero en un lienzo en blanco.
* **[!UICONTROL Exportar HTML]**: descargue el contenido del lienzo visual en su sistema local en formato HTML empaquetado como archivo zip.
