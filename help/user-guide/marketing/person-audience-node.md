---
title: Nodo de Recorrido de Audiencia de persona
description: Configure el nodo de audiencia de persona en Journey Optimizer B2B para especificar qué perfiles introducen un recorrido mediante listas dinámicas de personas o audiencias basadas en eventos.
TQID: 'https://experienceleague.adobe.com/WqM-yLPadt6lBFtqJOGUxDtk0fm6n6S29wQTRSWB8fY'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2:
  - id: 46e599c6-e20f-5f67-9824-93415016f66b
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 0%

---

# Nodo de audiencia de persona

El nodo _audiencia de persona_ especifica qué perfiles de persona entran en el recorrido. Cuando [crea un recorrido de persona](./person-journeys.md), el recorrido siempre comienza con un nodo de audiencia de persona que define su entrada. El nodo de audiencia de persona puede tener uno de estos dos tipos de entrada de audiencia: una lista dinámica de personas o un déclencheur de eventos.

Si la lista de personas dinámicas que necesita para el recorrido de personas no existe, [cree la lista de personas](../audiences/people-lists.md#create-a-people-list) y, a continuación, configure el nodo de audiencia de persona.

_Para configurar la audiencia de recorrido :_

1. Haga clic en el nodo **[!UICONTROL Audiencia de personas]**.

   Esta acción muestra las propiedades del nodo a la derecha.

   ![Nodo de recorrido de audiencia de persona](./assets/person-audience-node-properties.png){width="600" zoomable="yes"}

1. Utilice una de las siguientes opciones de configuración de audiencia para la audiencia de persona:

   * **[!UICONTROL Lista dinámica]**: use una lista de personas dinámica y basada en reglas. Las reglas de la lista se evalúan durante el tiempo de ejecución del recorrido para calificar a los miembros del recorrido. Las personas que posteriormente no cumplan los requisitos para la lista dinámica no se eliminarán del recorrido. Consulte _[Listas dinámicas](../audiences/people-lists.md#dynamic-lists)_.

   * **[!UICONTROL Audiencia de eventos]**: use una audiencia de eventos para definir la audiencia de recorrido en función de los eventos calificados. Defina los miembros de la audiencia mediante el filtrado de perfil de persona y la entrada de recorrido de déclencheur mediante criterios de evento. Ver _[audiencias basadas en eventos](../audiences/event-based-audiences.md)_.