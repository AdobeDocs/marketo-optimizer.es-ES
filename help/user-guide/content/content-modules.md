---
title: Módulos de contenido
description: Aprenda a añadir y personalizar módulos para correos electrónicos, páginas de aterrizaje, fragmentos visuales y plantillas de correo electrónico. Utilice diseños preparados para crear diseños de contenido coherentes.
feature: Content Design Tools
role: User
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
source-git-commit: 73e54767086a103c11dce78a0295ad435c07f2c0
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 1%
---
# Módulos de contenido

Use módulos en [!DNL Adobe Marketo Optimizer] para ensamblar contenido de diseños preparados. Cada módulo combina [estructura](./structure-components.md) y [componentes de contenido](./content-components.md) con contenido predeterminado que reemplaza por su propio texto, imágenes y vínculos.

A diferencia de los componentes de contenido individuales, los módulos proporcionan secciones completas como encabezados, banners, tarjetas y pies de página. Agregue un módulo al lienzo y, a continuación, personalice sus componentes en lugar de crear cada sección a partir de un espacio vacío.

Los módulos son diferentes de [fragmentos visuales](./fragments.md). Un módulo forma parte del contenido que está diseñando. Un fragmento visual es un recurso de contenido guardado que puede reutilizar en correos electrónicos y plantillas de correo electrónico.

## Pestaña Módulos

Use la ficha **[!UICONTROL Módulos]** en el espacio de diseño visual para cualquiera de los siguientes tipos de contenido:

* Correo electrónico: consulte [_Creación de contenido de correo electrónico_](./email-authoring.md).
* Página de aterrizaje: consulte [_Diseño de página de aterrizaje_](./landing-page-design.md).
* Fragmento visual: consulte [_Creación de fragmentos_](./fragment-authoring.md).
* Plantilla de correo electrónico - Consulte [_Crear plantillas de correo electrónico_](./templates-create.md#build-new).

![Categorías de módulos mostradas junto al lienzo de diseño visual](../../assets/modules-left-panel.png){width="600" zoomable="yes"}

## Categorías de módulo

Expanda una categoría para elegir un diseño. Estos diseños proporcionan diferentes disposiciones para el contenido de la sección, como una, dos o tres columnas.

| Categoría | Utilice |
| --- | --- |
| [!UICONTROL Encabezados] | Introduzca su contenido con un logotipo, vínculos de navegación y texto introductorio. |
| [!UICONTROL Héroe] | Resalte un anuncio o una promoción con una sección de banner. |
| [!UICONTROL Testimonio] | Presente las comillas del cliente en una sección con estilo. |
| [!UICONTROL Tarjetas] | Organizar productos, artículos u otros elementos de contenido en una cuadrícula. |
| [!UICONTROL Equipos] | Presente a los integrantes del equipo, autores o oradores con fotos, nombres y funciones. |
| [!UICONTROL Pies de página] | Finalice el contenido con vínculos de navegación, vínculos sociales y texto legal. |

## Añadir y personalizar módulos

Comience con un módulo que coincida con la sección que desea crear y, a continuación, adapte su contenido y estilo. Reemplace los vínculos y el texto predeterminados por el contenido apropiado para su canal.

>[!NOTE]
>
>Para los correos electrónicos de marketing, incluya un vínculo de no participación y [compruebe las alertas por correo electrónico](../marketing/email-channel.md#alerts) antes de publicar el correo electrónico.

1. Abra el correo electrónico, la página de aterrizaje, el fragmento visual o la plantilla de correo electrónico en el espacio de diseño visual.

   A la izquierda del lienzo, se muestra la ficha **[!UICONTROL Módulos]** de forma predeterminada.

1. Para revisar los diseños disponibles, expanda una categoría.

   También puede utilizar el campo de búsqueda para buscar un módulo por su nombre.

1. Arrastre un módulo al lienzo.

   ![La lista de módulos se filtra mediante la búsqueda y se arrastra un módulo al lienzo.](../../assets/modules-search-drag.png){width="600" zoomable="yes"}

1. Revise los elementos dentro del módulo.

   Cada módulo incluye contenido predeterminado que puede editar. Haga clic en el icono _Árbol de navegación_ ( ![Icono del árbol de navegación](../assets/do-not-localize/icon-navigation-tree.svg) ) a la izquierda del lienzo para mostrar la estructura y los elementos en el módulo.

   ![El árbol de navegación muestra la estructura y los elementos del módulo seleccionado.](./assets/modules-navigation-tree.png){width="600" zoomable="yes"}

1. Seleccione un elemento en el módulo para personalizarlo.

   Puede reemplazar el texto predeterminado, elegir imágenes de los recursos y actualizar los vínculos del contenido.

   Use las fichas **[!UICONTROL Configuración]** y **[!UICONTROL Estilos]** para ajustar el componente seleccionado.

   ![Componente de texto seleccionado en el módulo con las opciones de estilos mostradas](../../assets/modules-select-element-styles.png){width="600" zoomable="yes"}

1. Para agregar otro elemento, seleccione la ficha **[!UICONTROL Componentes]** y arrastre un [componente de contenido](./content-components.md) al módulo.

   Si agrega un componente a la estructura del módulo, heredará el estilo del módulo de forma predeterminada. Ajuste sus estilos según sea necesario.

   ![Componente de texto arrastrado a la estructura del módulo con texto de marcador de posición con formato mostrado](./assets/modules-select-element-add-component.png){width="800" zoomable="yes"}

1. Seleccione **[!UICONTROL Guardar]** para guardar los cambios.

>[!NOTE]
>
>Cuando se aplica un tema de marca al contenido del correo electrónico, los módulos heredan sus estilos. Elija el modo de estilo cuando [diseñe un correo electrónico desde cero](./email-authoring.md#design-from-scratch).

## Reutilización del contenido de módulo personalizado

Para generar contenido de módulo reutilizable, [cree un fragmento visual](./fragments.md#create-fragments) y agregue y personalice módulos en el espacio de diseño del fragmento. Guarde y publique el fragmento para que esté disponible para su uso en correos electrónicos y plantillas de correo electrónico.

Luego [inserta el fragmento](./fragments.md#add-to-content) en otros correos electrónicos o plantillas de correo electrónico.
