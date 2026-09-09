---
title: Escuchar un nodo de evento
description: 'Configuración de la escucha de nodos de evento en Marketo Optimizer: establezca déclencheur de evento, aplique filtros opcionales y haga avanzar a las personas cuando se produzcan actividades o cambios en los datos.'
TQID: 'https://experienceleague.adobe.com/6v3i6M-Hhr2RAWrS68WaEVb8VJEzJZbD7vXOJOsjgc8'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 354
ht-degree: 5%

---

# Escucha de un nodo de evento

Agregue el nodo _Listen for an event_ para mover la audiencia hacia adelante al siguiente paso del recorrido cuando se produzca un evento.

## Déclencheur de eventos {#event-triggers}

Puede generar déclencheur en torno a [!DNL Marketo Engage] actividades, como:

* Rellena formulario: se activa cuando una persona envía un formulario [!DNL Marketo Engage] en su página de aterrizaje.
* Página web de visitas: se activa cuando un posible cliente ve una página web rastreada (puede especificar direcciones URL exactas o utilizar caracteres comodín).
* Vínculo de clics: Se activa cuando se hace clic en un vínculo rastreado en un correo electrónico de marketing.
* Cambios en el valor de los datos: se activa cuando se actualiza un campo específico (como el estado del posible cliente, la puntuación o el sector) en el registro de una persona.
* Campaña solicitada: a menudo se utiliza para integraciones de API o ganchos web, este déclencheur inicia una campaña cuando otro programa o servicio web la llama.
* Se cambia la puntuación: se activa cuando la puntuación del posible cliente de un individuo aumenta o disminuye más allá de un determinado umbral.
* Pulsación móvil: Se activa en campañas inteligentes de marketing móvil cuando se interactúa con una notificación push en un dispositivo.

## Filtros de eventos {#event-filters}

| Filtros | Descripción |
| ------- | ----------- |
| Historial de actividades > Correo electrónico | Actividades de correo electrónico basadas en condiciones que se evalúan mediante uno o varios mensajes de correo electrónico seleccionados: <li>Hizo clic en el vínculo del correo electrónico <li>Abrió el email |
| Historial de actividades > Valor de los datos cambiado | Se ha producido un cambio de valor en un atributo de persona seleccionado. Estos tipos de cambio incluyen: <li>Nuevo valor <li>Valor anterior <li>Razón <li>Origen <li>Fecha de la actividad <li> Mín. número de veces |

## Adición de un nodo de evento {#add-event-node}

1. Navegue hasta el lienzo de recorrido.

1. Haga clic en el icono de signo más (**+** ) en una ruta y elija **[!UICONTROL Escuchar un evento]**.

   ![Haga clic en agregar icono en la ruta de recorrido](./assets/person-journey-canvas-add-node.png){width="200"}

1. En las propiedades del nodo, a la derecha, haga clic en **[!UICONTROL Agregar criterios de evento]**.

1. En el cuadro de diálogo _[!UICONTROL Editar evento]_, agregue los eventos al déclencheur.

   ![Editar evento: déclencheur de evento](./assets/edit-event-triggers.png){width="600" zoomable="yes"}

1. (Opcional) Seleccione la ficha **[!UICONTROL Filtros]** en el cuadro de diálogo y agregue criterios de filtrado para los déclencheur.

1. Haga clic en **[!UICONTROL Editar evento]** y defina los detalles del evento.

   ![Editar evento: filtrado de eventos](./assets/edit-event-filters.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Guardar]**.

<!--
1. If needed, set the **[!UICONTROL Timeout]** option to limit the time period to listen for the event.

   >[!NOTE]
   >
   >The journey ends after a timeout unless you define a timeout path, where you can add other nodes.

   Enable the **[!UICONTROL Timeout]** option and select the duration for which the journey waits for an event to occur before it times out.

   You can choose to end the path here or take a different course of action by setting another path. To create a new path in the journey where you can add actions and events applicable to accounts when the event does not occur, select the **[!UICONTROL Set timeout path]** check box.

   ![Journey event node - set timeout path](assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}
-->

>[!NOTE]
>
>La funcionalidad de tiempo de espera para Escuchar para un nodo de evento no funciona actualmente. Está planificado para una versión posterior.

