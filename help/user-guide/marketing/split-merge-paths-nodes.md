---
title: Dividir y combinar nodos de rutas
description: Aprenda a utilizar nodos de rutas divididas y combinadas en recorridos de persona para segmentar a las personas en rutas distintas en función de condiciones definidas y, a continuación, reunirlas en un punto común aguas abajo.
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# Dividir y combinar nodos de rutas

Utilice los nodos de rutas divididas y combinadas en recorridos de persona para segmentar a las personas en rutas distintas en función de las condiciones definidas y, a continuación, vuelva a unir esas rutas para que el recorrido pueda continuar. Las rutas divididas le permiten adaptar las acciones y los eventos a segmentos de audiencia específicos, mientras que las rutas de combinación reúnen esos segmentos en un punto común descendente.

## Dividir nodos de rutas

Utilice los nodos divididos para segmentar a las personas según las condiciones que defina. Cree rutas para la lista de audiencias según las condiciones, defina cada ruta con nodos de acción y evento para el segmento y, a continuación, combine las rutas y continúe con el recorrido.

Un nodo de Rutas divididas define una o más rutas segmentadas en función de los filtros de personas.

<!-- A split based on a people filter is automatically closed with a merge paths node so that all people can move forward to the next step. Split by people paths can include only people actions. These paths cannot be split again and automatically join back. _not currently true_ -->

_**Funcionamiento de un nodo de ruta dividida por personas**_

* La evaluación de cada ruta es de arriba abajo. Si una persona coincide para la primera y la segunda ruta, solo continúa por la primera ruta.
* El nodo admite la definición de una ruta de acceso de _Otras personas_, donde puede agregar acciones o eventos para las personas que no coincidan con uno de los segmentos o rutas definidos.

### Filtros coincidentes

Para cada ruta definida para el nodo, utilice los siguientes tipos de filtros para hacer coincidir personas según una o más condiciones:

* Historial de actividades: puede definir una ruta según la actividad de la persona relacionada con lo siguiente:

  * Mensajes de correo electrónico
  * Cambio en el valor de los datos

* Atributos de persona: defina una condición según los atributos de una persona, como país, cargo, persona derivada o pertenencia a una lista.

### Adición de un nodo de rutas divididas

1. Navegue hasta el lienzo de recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Dividir rutas]**.

   ![Haga clic en agregar icono en la ruta de recorrido](./assets/person-journey-canvas-add-node.png){width="200"}

1. Para definir una condición aplicable a _[!UICONTROL Ruta 1]_, haga clic en **[!UICONTROL Aplicar condición]**.

1. En el editor de condiciones, añada uno o más filtros para definir la ruta dividida.

   * Arrastre y suelte cualquiera de los filtros de personas desde la navegación izquierda y complete la definición de la coincidencia.

   * Ajuste las condiciones aplicando la **[!UICONTROL lógica de filtro]** en la parte superior. Puede elegir hacer coincidir todas las condiciones o cualquier condición.

     <!-- ![Split path node - conditions person filter logic](./assets/node-split-conditions-people.png){width="700" zoomable="yes"} -->

   * Haga clic en **[!UICONTROL Finalizado]**.

1. Para agregar más rutas, haga clic en **[!UICONTROL Agregar ruta]** y repita los pasos anteriores para agregar las condiciones aplicables a la ruta.

   También puede etiquetar cada ruta en función de estas condiciones o utilizar las etiquetas predeterminadas.

1. Si es necesario, reordene las rutas según la prioridad que desee para la división.

   El filtrado de rutas se evalúa en orden descendente. Cada persona continúa por el primer camino que coincida.

   Haga clic en las flechas arriba y abajo en la parte superior derecha de cada tarjeta de ruta para moverla hacia arriba o hacia abajo en la lista de rutas.

   <!-- ![Split path node - reorder paths](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"} -->

1. Habilite la opción **[!UICONTROL Otras personas]** para agregar una ruta predeterminada para las personas que no coinciden con las rutas definidas.

   Cuando esta opción no está habilitada, las personas que no coinciden con un segmento o ruta definida pasan la división y continúan con el siguiente paso del recorrido.

Cuando haya definido condiciones para cada ruta, puede añadir nodos de acción o de evento que desee aplicar a las personas de una ruta.

## Combinar nodos de rutas

1. Vaya al lienzo de recorrido y busque el nodo de rutas divididas con dos o más rutas.

   Cada ruta debe tener una combinación de acciones y eventos en cada ruta.

1. Haga clic en el icono de signo más ( **+** ) al final de cualquiera de estas rutas y elija **[!UICONTROL Combinar rutas]** entre las opciones que se muestran.

1. En las propiedades del nodo a la derecha, seleccione las rutas que desee combinar.

   <!-- ![Journey node - merge paths](./assets/node-merge-select-paths.png){width="600" zoomable="yes"} -->

   En este punto, las rutas se combinan para que las personas de las rutas seleccionadas se combinen en una sola ruta que pueda continuar avanzando a través del recorrido.

1. Si es necesario, puede anular la combinación de rutas volviendo a las propiedades del nodo de rutas de combinación y desactivando la casilla de verificación de las rutas que desee eliminar.