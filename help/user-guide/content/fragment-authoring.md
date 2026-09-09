---
title: Creación de fragmentos
description: 'Cree fragmentos de contenido reutilizables con las herramientas de diseño visual: añada estructura, recursos, personalización, contenido condicional y seguimiento de URL vinculado para correos electrónicos y plantillas en Marketo Optimizer.'
TQID: 'https://experienceleague.adobe.com/KbnYkUMVfjBv5ST55WwAqYiMDkynwSw4BKIP0bsE-DI'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 203
ht-degree: 3%

---

# Creación de fragmentos

Después de [crear un fragmento](./fragments.md#create-fragments), use el espacio de diseño visual para crear la estructura y los componentes de contenido del fragmento.

## Añadir estructura y contenido {#design-fragment}

{{$include /help/_includes/content-design-components-prime.md}}

## Añadir recursos {#add-assets}

En el espacio de diseño visual, seleccione el icono _Assets_ ( ![Assets icon](../assets/do-not-localize/icon-assets-me.svg) ) en la barra de navegación izquierda para examinar y seleccionar recursos de imagen de la biblioteca de recursos [!DNL Marketo Optimizer].

Para ver los pasos para seleccionar, reemplazar o cargar recursos de imagen, consulte [Usar recursos para la creación de contenido](./digital-asset-management.md#assets-authoring).

## Desplazamiento por las capas, la configuración y los estilos {#navigate-layers-settings-styles}

{{$include /help/_includes/content-design-navigation.md}}

## Personalización del contenido {#personalize-content}

[!DNL Marketo Optimizer] utiliza la sintaxis de Handlebars para la personalización. Los tokens se sustituyen en el momento del envío con valores de los datos de perfil de cada destinatario.

_Para agregar personalización :_

1. Seleccione el componente de texto y haga clic en el icono _Agregar personalización_ ( ![Icono de personalización](../assets/do-not-localize/icon-personalize.svg) ) de la barra de herramientas.
1. En el cuadro de diálogo de personalización, examine el árbol de esquema de la izquierda y seleccione un atributo de perfil. El editor inserta la expresión Handlebars correspondiente; por ejemplo, `{{profile.firstName}}`.
1. Agregue un valor de reserva para controlar los datos que faltan, si es necesario; por ejemplo, `{{profile.firstName | default: "there"}}`.
1. Haga clic en **[!UICONTROL Confirmar]** o **[!UICONTROL Insertar]**. La expresión aparece en línea en el campo.

Para obtener más información sobre las herramientas y la sintaxis del editor de expresiones, consulte [Editor de Personalization](./personalization-expressions.md).

## Editar seguimiento de URL vinculadas {#edit-linked-url-tracking}

{{$include /help/_includes/content-design-links.md}}
