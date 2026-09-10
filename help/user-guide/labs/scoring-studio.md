---
title: Puntuación de Studio
description: Obtenga información sobre Scoring Studio en Adobe Marketo Optimizer, incluida la lista de modelos, lienzo, columnas de dimensión, tarjetas de señal, segmentos de posibles clientes y publicación.
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 1650dadf-b034-5ac9-a309-77ad1e2f5035
source-git-commit: 96a923c923a6290b9d90e4ffc8e161d78f029c47
workflow-type: tm+mt
source-wordcount: 897
ht-degree: 2%

---


# Puntuación de Studio

Scoring Studio incluye una lista de modelos, un lienzo editable para cada modelo y la [interfaz de chat de Coworker](../agents/chat-interface.md). Utilice el lienzo para revisar o ajustar dimensiones y señales directamente, mientras que Coworker continúa proponiendo cambios en el lenguaje natural a su lado. Para obtener información acerca de cómo crear un modelo a partir de una solicitud, vea [_Crear modelos de puntuación personalizados_](../agents/lead-scoring-model.md).

## Lista de modelos {#model-list}

La lista de modelos es la vista de aterrizaje de Scoring Studio. Muestra todos los modelos de puntuación de la instancia [!DNL Marketo Optimizer] como filas de una tabla o como tarjetas si cambia a la vista de cuadrícula.

| Columna | Descripción |
| --- | --- |
| Nombre | Seleccione el nombre de un modelo para abrirlo en el lienzo. |
| Estado | _[!UICONTROL Activo]_, _[!UICONTROL Borrador]_ o _[!UICONTROL Archivado]_. |
| Dimensiones | Número de dimensiones del modelo. |
| Señales | Número de señales del modelo. |
| Última modificación | La fecha en la que se cambió el modelo por última vez. |
| Última modificación de | La última persona que cambió el modelo. |
| Creado el | La fecha de creación del modelo. |
| Creado por | La persona que creó el modelo. |

![La lista de modelos de Scoring Studio muestra los modelos de puntuación activos con sus dimensiones, señales y detalles modificados por última vez.](./assets/scoring-studio-ui.png){width="800" zoomable="yes"}

Utilice el campo de búsqueda para buscar un modelo por nombre o filtre la lista por estado. Seleccione el **[!UICONTROL menú Más]** de una fila para **[!UICONTROL editar]**, **[!UICONTROL duplicar]**, **[!UICONTROL archivar]** o **[!UICONTROL eliminar]** un modelo.

Un modelo activo es de solo lectura. Para cambiarlo, duplique y edite el duplicado. A continuación, archive el original y publique la copia modificada.

## Lienzo de modelo {#model-canvas}

Al seleccionar el nombre de un modelo, se abre en el lienzo. Cada modelo abierto aparece como su propia pestaña, por lo que puede trabajar en varios modelos. El lienzo está organizado en fichas, incluidas **[!UICONTROL Reglas]** y **[!UICONTROL Posible cliente]**.

En la ficha **[!UICONTROL Reglas]**, cada dimensión del modelo es una columna en el lienzo. Cada encabezado de columna muestra el nombre de dimensión y su total de puntos con respecto a su límite, por ejemplo `20 / 30 pts`, con una barra de progreso que se rellena a medida que sus señales aportan puntos.

![El lienzo de la pestaña Reglas muestra tres columnas de dimensión, Participación por correo electrónico, Ajuste de perfil y Actividad reciente, cada una con tarjetas de señal y puntos.](./assets/scoring-studio-model-rules-tab.png){width="700" zoomable="yes"}

Dentro de cada dimensión, cada señal aparece como una tarjeta que muestra su nombre, su valor de punto y su frecuencia coincidente (por ejemplo, `1 time / day`) o `Static` para señales basadas en atributos que no dependen de la actividad.

Cuando Coworker detecta un patrón en varias actividades, puede combinarlo en una sola tarjeta de señal compuesta que resuma cada condición.

## Configuración de una señal {#configure-signal}

Para revisar o cambiar una señal, siga estos pasos.

1. Seleccione **[!UICONTROL Editar borrador]**.

1. Seleccione una tarjeta de señal en el lienzo.

   El panel de propiedades se abre en el lado derecho del lienzo.

   ![El lienzo de la ficha Reglas muestra una tarjeta de señal seleccionada y su panel de propiedades con el tipo de señal, el tipo de actividad, las condiciones y los puntos.](./assets/scoring-studio-model-selected-signal.png){width="700" zoomable="yes"}

1. Seleccione el icono **[!UICONTROL Editar]** ( ![Editar icono](../assets/do-not-localize/icon-react-edit.svg) ) y, a continuación, actualice las propiedades de la señal:

   * En **[!UICONTROL Señal]**, confirme el tipo de señal (una actividad o un atributo) y la actividad o atributo específico que puntúa.

   * En **[!UICONTROL Activar esto el]**, establezca las condiciones que deben coincidir.

     Agregue los elementos que desee usar, como páginas específicas, y si **[!UICONTROL Cualquiera de]** o **[!UICONTROL Todos de]** las condiciones deben ser verdaderas.

   * En **[!UICONTROL Puntos]**, defina cuántos puntos aporta la señal.

     De manera opcional, establezca un **[!UICONTROL Límite]** para limitar la cantidad de puntos que puede aportar por persona. El compañero muestra un rango de puntos sugerido basado en las otras señales del modelo.

   * Para señales basadas en actividad, establezca la **[!UICONTROL Frecuencia]** necesaria antes de que la señal otorgue puntos.

     De manera opcional, establezca un porcentaje de **[!UICONTROL Decaimiento]** que reduzca los puntos de la señal después de un número determinado de días.

   * Habilite la opción **[!UICONTROL Evite anotar las mismas acciones dos veces]** para otorgar puntos solo una vez por persona, sin importar cuántas veces suceda la actividad.

     Desactive la opción para asignar puntos cada vez que se produzca la actividad. Esta opción está activada de forma predeterminada.

1. Seleccione **[!UICONTROL Guardar]** para aplicar los cambios y volver al lienzo.

## Segmento de posible cliente {#lead-segment}

Cada modelo de puntuación puntúa un segmento de posible cliente, una referencia a una lista de personas existente en lugar de a las reglas definidas dentro de Scoring Studio. Cuando el Compañero de trabajo crea un modelo, selecciona una lista coincidente o crea una nueva.

Para cambiar la lista, selecciona la ficha **[!UICONTROL Posible cliente]** y, a continuación, selecciona **[!UICONTROL Cambiar]** junto al segmento de posibles clientes.

![La ficha Posible cliente muestra la tarjeta de segmento de clientes potenciales con una lista de personas a las que se hace referencia, un vínculo Ver lista de personas y un vínculo Cambiar.](./assets/scoring-studio-model-lead-tab.png){width="700" zoomable="yes"}

Un segmento de posibles clientes utiliza uno de los dos tipos de lista:

* **Lista estática**: un conjunto fijo de personas capturadas cuando se creó la lista.
* **Lista inteligente**: una lista que vuelve a evaluar sus reglas de pertenencia cada vez que se ejecuta el modelo, por lo que el segmento siempre refleja los criterios de la lista.

La vista previa del modelo muestra el nombre del segmento, su recuento de miembros y un vínculo **[!UICONTROL Ver lista de personas]** que abre la lista directamente. Para obtener más información acerca de la administración de listas, vea [_Listas de personas_](../audiences/people-lists.md).

Si la lista a la que se hace referencia está vacía o se elimina posteriormente, el modelo deja de puntuar en lugar de volver a caer en toda la audiencia. No se puntúan posibles clientes hasta que asigne una lista válida que no esté vacía.

Debajo del segmento de posibles clientes, la tarjeta **[!UICONTROL Nombre del campo de puntuación]** muestra el atributo de posible cliente al que el modelo escribe su puntuación. De forma predeterminada, el nombre de campo coincide con el nombre del modelo. Seleccione **[!UICONTROL Editar]** para cambiarle el nombre.

## Publicación y programación {#publish-schedule}

Cuando el modelo esté listo, seleccione **[!UICONTROL Publicar]**. Elija la frecuencia con la que el modelo puntúa su audiencia: diaria, semanal o mensual.

Para ver el proceso de publicación completo, incluido cómo [!DNL Marketo Optimizer] aprovisiona automáticamente un campo de puntuación, consulte [_Publicar un modelo de puntuación_](../agents/lead-scoring-model.md#publish-model).
