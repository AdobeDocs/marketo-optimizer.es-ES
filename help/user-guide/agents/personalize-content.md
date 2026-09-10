---
title: Personalizar contenido de correo electrónico por persona
description: Utilice la habilidad Personalization de contenido en Marketo Optimizer para convertir un correo electrónico en variantes basadas en datos o en personas. Personalizar o analizar correos electrónicos.
TQID: 'https://experienceleague.adobe.com/9fa1wfsHH6h46jJ-slLxMpB6fud1VHgmiWxbao-bWvo'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2:
  - id: 1650dadf-b034-5ac9-a309-77ad1e2f5035
  - id: 46e599c6-e20f-5f67-9824-93415016f66b
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 1236
ht-degree: 0%

---


# Personalizar contenido de correo electrónico por persona

La habilidad _Personalization de contenido_ convierte un correo electrónico en variantes basadas en datos y basadas en personas, por lo que no tiene que crear un correo electrónico independiente para cada audiencia. En lugar de enviar un mensaje después de un evento, la aptitud resuelve la audiencia en [cohortes de personalidades derivadas](../audiences/personas.md), muestra perspectivas y genera variantes personalizadas. Cada variante se guarda como contenido condicional dentro de un solo correo electrónico, por lo que cada persona recibe automáticamente la versión que coincide con su perfil cuando un recorrido la envía.

* **Habilidad** - `content-personalization`
* **Invocación** - Desde la [interfaz de chat](./chat-interface.md), describe una audiencia de destino para un nuevo correo electrónico o selecciona **[!UICONTROL Personalizar este correo electrónico]** o **[!UICONTROL Analizar este correo electrónico]** en un correo electrónico existente en un [Enviar nodo de correo electrónico](../marketing/action-nodes.md)
* **Lee/escribe en** - [!DNL Marketo Optimizer]

## Conceptos clave {#key-concepts}

| Término | Definición |
|---|---|
| **Cohorte personal** | Un grupo de personas que comparten un [perfil derivado](../audiences/personas.md), como _CXO/EVP_ o _colaborador individual_. |
| **Segmento** | Grupo de personas definidas según cualquier criterio, como persona, sector o nivel de participación. Una cohorte de persona es un segmento definido específicamente por una persona derivada compartida. |
| **Grupo de destino** | La audiencia que describe en lenguaje natural. La aptitud lo resuelve en cohortes de personas coincidentes. |
| **Insight** | Un hallazgo basado en datos sobre la mensajería, el posicionamiento o el tono que mejor se adapta a una cohorte personal, extraído de sus propios datos. |
| **Variante** | Una versión personalizada de las secciones de correo electrónico que eligió personalizar, generada para una cohorte de personas. |
| **Correo electrónico personalizado de IA** | El único correo electrónico guardado que agrupa todas las variantes como [contenido condicional](../content/conditional-content.md) bloques. |
| **Auditoría de correo electrónico** | Una revisión de un correo electrónico existente en relación con cada uno de los segmentos del grupo destinatario, que muestre qué resuena y qué mejorar para cada persona antes de personalizar. |

## Requisitos previos {#prerequisites}

* Acceso a [!DNL Marketo Optimizer] con Compañero de trabajo habilitado.
* [Personas derivadas](../audiences/personas.md) resueltas en sus datos. La aptitud se basa en estas clasificaciones para crear cohortes de personas. La compatibilidad con Persona personalizada está planificada para una versión futura.
* Suficientes datos históricos para las perspectivas. Si no hay perspectivas disponibles para una cohorte de personas, la aptitud le indica que los datos son insuficientes y vuelve a las prácticas recomendadas generales para ese personaje.
* Una [plantilla de correo electrónico](../content/templates.md) o un correo electrónico existente al que hace referencia un nodo de acción [_Enviar correo electrónico_](../marketing/action-nodes.md).
* Un [recorrido de persona](../marketing/person-journeys.md) que contiene el nodo de acción _Enviar correo electrónico_ usado para enviar el correo electrónico personalizado.

## Creación y personalización de un correo electrónico a partir de una plantilla {#create-personalize-from-template}

Este flujo crea un nuevo correo electrónico y lo personaliza en la misma conversación.

1. **Proporcione el contenido.** Cargue una descripción breve del contenido o describa el contenido que desee en lenguaje natural.

1. **Seleccione una [plantilla](../content/templates.md)** de su biblioteca de plantillas.

1. **Revisar el borrador.**

   El compañero asigna el contenido a la plantilla y genera un borrador de correo electrónico. Puede realizar ediciones de texto básicas en línea.

   >[!WARNING]
   >
   >Durante la creación, solo están disponibles en línea las ediciones de texto básicas. Para realizar ediciones avanzadas, guarde el correo electrónico y ábralo en [espacio de diseño visual](../content/email-authoring.md).

1. **Describa el grupo destinatario** en lenguaje natural.

1. **Revisar las cohortes de personas resueltas**.

   El compañero inspecciona sus datos y devuelve las cohortes de personas que coinciden con su descripción, con un recuento para cada una. Revise la descripción del grupo de destino e inténtelo de nuevo si es necesario.

1. **Confirmar el grupo de destino**.

   A continuación, el compañero recupera información de cada cohorte de personalidad resuelta.

1. **Seleccione las secciones que desea personalizar**, como la línea de asunto o una sección del cuerpo, y revise las variantes generadas.

   Volver a generar una variante si no cabe. El número de cohortes de personas no es fijo. Depende del grupo destinatario y de los datos.

1. **Guarde el correo electrónico**.

   Todas las variantes se almacenan en un correo electrónico personalizado de IA, no como correos electrónicos independientes.

<!-- screenshot: Coworker chat panel showing the resolved persona cohorts with counts, and the "Personalized variants" review grid -->

## Analizar un correo electrónico existente {#analyze-existing-email}

En un nodo [_Enviar correo electrónico_ de recorrido](../marketing/action-nodes.md) que hace referencia a un correo electrónico existente, el panel **[!UICONTROL Realizar una acción]** muestra el nombre del correo electrónico con dos opciones: **[!UICONTROL Personalizar este correo electrónico]** y **[!UICONTROL Analizar este correo electrónico]**.

<!-- screenshot: Send Email node "Take an action" panel showing the email name and the Personalize this email / Analyze this Email options -->

Seleccione **[!UICONTROL Analizar este correo electrónico]** para ejecutar una auditoría de correo electrónico:

1. **Describa el grupo destinatario** para el que desea personalizar, en términos de su personalidad.

   Por ejemplo _Personas en los roles de marketing_ o _Personas en los roles de liderazgo_.

1. **Revisar la auditoría de correo electrónico.**

   El compañero resuelve su descripción en segmentos personales y muestra una tarjeta de **auditoría de correo electrónico** en la que se enumera cada segmento. A continuación, revisa el correo electrónico comparándolo con cada uno de ellos para resaltar qué es lo que más impacto tiene y qué mejorar.

1. El compañero pregunta qué hacer a continuación, incluyendo **[!UICONTROL Ver auditoría sección por sección]** y **[!UICONTROL Personalizar este correo electrónico]**.

1. Seleccione **[!UICONTROL Ver auditoría sección por sección]** para abrir una vista de **_análisis de correo electrónico_** con un selector de persona y recomendaciones específicas para cada sección.

   Cada sección muestra cuántos cambios se recomiendan y cada perfil muestra un recuento de recomendaciones, como `4 recommendations for SVP/VP`. También puedes aplicar las recomendaciones directamente ingresando _personalizar_ en el chat.

1. En la auditoría, seleccione **[!UICONTROL Personalizar este correo electrónico]** para aplicar las perspectivas y generar variantes.

   Consulte la siguiente sección [_Personalizar un correo electrónico existente_](#personalize-existing-email).

<!-- screenshot: Email analysis view with persona selector, per-section "N changes" badges, and "what needs work" recommendations -->

## Personalizar un correo electrónico existente {#personalize-existing-email}

Seleccione **[!UICONTROL Personalizar este correo electrónico]** en un nodo de acción _Enviar correo electrónico_ o continúe desde una [auditoría de correo electrónico](#analyze-existing-email) para personalizar un correo electrónico que ya haya creado.

1. **Revisar las cohortes de personas resueltas.**

   El compañero inspecciona sus datos y devuelve las cohortes de personas que coinciden con su descripción, con un recuento para cada una. Revise la descripción del grupo de destino e inténtelo de nuevo si es necesario.

   Si ha llegado a este paso desde una auditoría de correo electrónico, Coworker continúa directamente desde las perspectivas de auditoría.

1. **Seleccione las secciones que desea personalizar** en la vista previa de correo electrónico, como la línea de asunto y secciones de contenido específicas, y confirme.

1. **Revisar las variantes generadas.**

   Además de persona, las variantes también pueden variar según el sector, por ejemplo un CXO en atención sanitaria en comparación con un CXO en servicios financieros. El compañero presenta una cuadrícula de **[!UICONTROL variantes personalizadas]**, una tarjeta por cohorte de persona, cada una con una línea de asunto, un titular, un cuerpo y una opción de **[!UICONTROL vista previa]**.

   Seleccione el icono _Información_ de una tarjeta para ver el insight detrás de esa variante (el personaje en el que se basa y el insight de participación que la formó) y vuelva a generar una variante si es necesario.

   Puede filtrar la cuadrícula por persona.

1. **Guardar el conjunto.**

   Haga clic en **[!UICONTROL Guardar]** y confirme. El compañero confirma que el correo electrónico ya está disponible en la biblioteca de IA y, a continuación, pregunta si desea aplicar también los cambios al correo electrónico original, lo que lo actualiza en su lugar.

<!-- screenshot: "Personalized variants" grid showing persona cards with subject, headline, body, Preview, and the info-icon insight tooltip -->

## Salida guardada y uso en un recorrido {#saved-output}

Independientemente del flujo desde el que comience, la personalización produce un único **correo electrónico personalizado de IA** almacenado en la biblioteca de IA. El correo electrónico contiene [contenido condicional](../content/conditional-content.md) bloques tecleados por persona. Para editar secciones, ábralo en [espacio de diseño visual](../content/email-authoring.md) y para obtener una vista previa de cómo se resuelve cada bloque con clave personal, usa **[!UICONTROL Simular contenido]**.

Para usar el correo electrónico en un recorrido, agrega un [nodo Enviar correo electrónico](../marketing/action-nodes.md) y selecciona **[!UICONTROL Correos electrónicos personalizados de IA]** en lugar de **[!UICONTROL Crear un correo electrónico]** y, a continuación, elige el correo electrónico guardado. Aplique la configuración y las reglas empresariales al nodo como de costumbre.

<!-- screenshot: Send Email node configuration with "AI Personalized Emails" selected and the saved email applied -->

## Comportamiento en tiempo de ejecución {#run-time-behavior}

Puede seleccionar un solo correo electrónico personalizado de IA en el recorrido, no una variante por audiencia. Cuando se ejecuta el recorrido, el correo electrónico se resuelve automáticamente en la variante que coincide con el perfil de cada destinatario. No elige una variante por destinatario.

## Limitaciones {#limitations}

| Limitación | Detalles |
|---|---|
| **personalidades personalizadas** | Aún no es compatible. La aptitud clasifica cohortes de personas de [personas derivadas](../audiences/personas.md) solo de forma predeterminada. |
| **Datos insuficientes para la información** | Si los datos no admiten un insight para una cohorte de personas, la aptitud se indica así y vuelve a las prácticas recomendadas generales para ese persona. |
| **Edición en línea durante la creación** | Solo las ediciones de texto básicas están disponibles en línea cuando [crea y personaliza un correo electrónico a partir de una plantilla](#create-personalize-from-template). Las ediciones avanzadas requieren [espacio de diseño visual](../content/email-authoring.md). |
| **Se requiere el punto de inicio** | La personalización de un correo electrónico requiere una plantilla o un correo electrónico existente al que haga referencia un nodo Enviar correo electrónico. |
