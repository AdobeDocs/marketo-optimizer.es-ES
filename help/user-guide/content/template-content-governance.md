---
title: Gobernanza de contenido para plantillas
description: Utilice la configuración de gobernanza en Marketo Optimizer para bloquear contenido en plantillas de correo electrónico en el nivel de estructura o componente y controlar lo que los autores de correo electrónico pueden editar.
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---


# Gobernanza de contenido para plantillas

El bloqueo de contenido permite a los autores de plantillas definir reglas de gobernanza que restringen qué partes de una plantilla de correo electrónico se pueden modificar cuando la plantilla se utiliza en un correo electrónico. Esto ayuda a los equipos de conformidad y marca a proteger los elementos clave de diseño, como encabezados, logotipos y contenido legal, al tiempo que permiten a los equipos de marketing personalizar el mensaje dentro de la estructura aprobada.

>[!NOTE]
>
>El bloqueo de contenido es una función de control en el nivel de editor. Controla lo que los autores pueden editar en el espacio de diseño de correo electrónico, pero no evita los cambios realizados a través de la API.

Solo los usuarios que tengan el permiso **[!UICONTROL Administrar plantillas de contenido]** pueden establecer la configuración de control.

## Habilitar gobernanza {#enable}

>[!NOTE]
>
>En esta versión de Beta, solo se admiten plantillas de correo electrónico.

1. Abra la plantilla en el espacio de diseño.
1. En el lienzo, haga clic en el componente **[!UICONTROL Cuerpo]** para seleccionarlo.
1. Seleccione el icono _Configuración_ en el panel derecho,
1. Alternar **[!UICONTROL Gobernanza]**.
1. Para **[!UICONTROL Mode]**, seleccione el tipo de control que desea aplicar:

   | Modo | Descripción |
   | ---- | ----------- |
   | **[!UICONTROL Bloqueo de contenido]** | Bloquear selectivamente estructuras o componentes específicos. Los autores pueden editar las áreas desbloqueadas. |
   | **[!UICONTROL Sólo lectura]** | Bloquee toda la plantilla. Los autores pueden aplicarlo a un correo electrónico, pero no pueden modificar ninguna parte de su contenido. |

1. Si ha seleccionado el modo Bloqueo de contenido, puede definir aún más cómo los usuarios pueden interactuar con la plantilla.

   Active la opción Habilitar adición de contenido y elija una de las siguientes opciones:

   * **[!UICONTROL Permitir la adición de estructura y contenido]**: los usuarios pueden agregar estructuras entre las existentes y agregar componentes de contenido o fragmentos dentro de estructuras editables.

   * **[!UICONTROL Permitir solo la adición de contenido]**: los usuarios pueden agregar componentes de contenido o fragmentos dentro de estructuras editables, pero no pueden agregar ni duplicar estructuras.

### Bloqueo de una estructura {#lock-structure}

1. En el lienzo, seleccione la estructura (diseño de columna) que desee proteger.
1. En el carril derecho, habilite la opción **[!UICONTROL Bloquear estructura]**.

Todo el contenido anidado en una estructura bloqueada se bloquea automáticamente. Para permitir que un componente específico dentro de una estructura bloqueada permanezca editable, seleccione el componente y habilite **[!UICONTROL Editable]** en el carril derecho.

De forma predeterminada, los autores no pueden eliminar una estructura bloqueada. Para permitir la eliminación, habilite la opción **[!UICONTROL Permitir eliminación]** en el carril derecho.

### Bloquear un componente {#lock-component}

En una estructura editable, puede bloquear componentes de contenido individuales.

1. Seleccione el componente en el lienzo.
1. En el carril derecho, habilite la opción **[!UICONTROL Bloquear contenido]** y elija el tipo de bloqueo:

   | Tipo de bloqueo | Descripción |
   | --------- | ----------- |
   | **[!UICONTROL Bloqueado]** | Evita las modificaciones de contenido y estilo. Los autores no pueden editar texto ni cambiar el aspecto del componente. |
   | **[!UICONTROL Solo contenido editable]** | Permite a los autores editar texto y contenido, pero evita cambios de estilo como colores, fuentes y espaciado. |
   | **[!UICONTROL Editable]** | Permite modificaciones completas incluso dentro de una estructura bloqueada. |

De forma predeterminada, los autores no pueden eliminar un componente bloqueado. Para permitir la eliminación, habilite la opción **[!UICONTROL Permitir eliminación]** en el carril derecho.

### Permitir adiciones de contenido {#allow-additions}

Al usar el modo **[!UICONTROL Bloqueo de contenido]**, puede permitir que los autores agreguen contenido nuevo a la plantilla mientras mantiene los elementos bloqueados protegidos:

1. Habilitar **[!UICONTROL Permitir la adición de contenido]**.
1. Elija si los autores pueden agregar estructuras y componentes de contenido o solo componentes de contenido.

## Identificar elementos bloqueados {#identify}

El **[!UICONTROL árbol de navegación]** en el carril izquierdo muestra iconos de candado y lápiz para ayudar a los autores a identificar rápidamente lo que pueden y no pueden modificar:

* Un **icono de candado** indica un elemento que está bloqueado.
* Un **icono de lápiz** indica un elemento que se puede editar.

Para mejorar aún más la visibilidad, habilite el botón de alternancia **[!UICONTROL Resaltar áreas editables]** para distinguir visualmente las áreas editables de las bloqueadas en el lienzo.

## Consideraciones

La configuración de gobernanza se guarda con la plantilla. Cualquier correo electrónico creado a partir de una plantilla controlada hereda su configuración de bloqueo en el momento en que se aplica. La actualización de la configuración de gobernanza en una plantilla no afecta a los correos electrónicos creados anteriormente a partir de ella.
