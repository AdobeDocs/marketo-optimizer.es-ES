---
title: Configuración por intención
description: Aprenda a configurar las ponderaciones de actividad que impulsan el modelo de puntuación por intención de persona, desde los valores predeterminados sugeridos por IA hasta la activación de un modelo de ponderación personalizado.
TQID: 'https://experienceleague.adobe.com/ZL9RJqD-OZkIgFMpwJ4Cz-FW-463w6OJyEHAe5uJuec'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2:
  - id: 1650dadf-b034-5ac9-a309-77ad1e2f5035
topic_v2:
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 1322
ht-degree: 2%

---


# Configuración por intención

Un único conjunto estandarizado de ponderaciones de la actividad no funciona entre los clientes. Lo que indica una intención real de compra varía según el negocio. Configure y active un modelo por intención para especificar lo que le importa, por ejemplo, si un formulario de relleno indica más que un clic de correo electrónico, en lugar de heredar un valor predeterminado global.

Las herramientas del panel **[!UICONTROL Configuración por intención]** controlan la cantidad de tiempo que cada actividad de posible cliente por intención cuenta en la puntuación por intención de una persona. Es la única entrada configurable en la puntuación por intención. Otros factores, como la relevancia del contenido, el deterioro y los umbrales, se administran por el sistema. Está disponible a través de la [aptitud de configuración por intención](../agents/intent.md#configure-model).

Abra el panel mediante uno de los dos métodos de la [interfaz de chat](../agents/chat-interface.md) de Coworker:

* Escriba el comando `/intent-configuration`.
* Haga clic en **[!UICONTROL +]**, seleccione **[!UICONTROL Usar una aptitud de agente]**, seleccione la ficha **[!UICONTROL Intención]** y, a continuación, haga clic en **[!UICONTROL Configuración de la intención]**.

![El panel de configuración por intención se abrió desde la interfaz de chat](./assets/intent-configuration-panel.png){width="700" zoomable="yes"}

## Vista de lista de modelos

Al aterrizar en el panel se muestra **[!UICONTROL la ponderación de puntuación por intención]**, con el recuento total de modelos debajo del título, un campo de búsqueda para filtrar por nombre y una tabla ordenable:

| Columna | Notas |
| --- | --- |
| [!UICONTROL Nombre] | Ordenable, orden predeterminado |
| [!UICONTROL Estado] | _[!UICONTROL Activo]_ (punto verde), _[!UICONTROL Borrador]_ (punto naranja), _[!UICONTROL Archivado]_ (punto gris) |
| [!UICONTROL Fecha de creación] | Abreviado, fecha completa al pasar el ratón por encima |
| [!UICONTROL Última actualización] | Abreviado, fecha completa al pasar el ratón por encima |
| [!UICONTROL Última actualización] | Nombre de usuario truncado, nombre completo al pasar el ratón por encima |

Solo un modelo puede ser _[!UICONTROL Activo]_ en cualquier momento y es el modelo el que impulsa la puntuación. Todos los demás modelos se encuentran en un estado de _[!UICONTROL Borrador]_ (en proceso de edición, aún no activo) o _[!UICONTROL Archivado]_ (un modelo anterior de _[!UICONTROL Activo]_, que se degrada automáticamente cuando se activa uno nuevo).

Haga clic en una fila para abrir la vista de detalles del modelo.

## Vista de detalles del modelo

La vista de detalles muestra el nombre del modelo, el distintivo de estado, la marca de tiempo guardada por última vez y una ruta de exploración que muestra **[!UICONTROL Ponderación de puntuación por intención]** y el nombre del modelo, en el que puede hacer clic para volver a la lista.

La vista de detalles enumera las actividades de intención del comprador y el nivel de importancia que cada una contribuye a la puntuación de intención de la persona. El catálogo de actividades es fijo y solo pueden cambiar los niveles. Estos niveles son independientes: no es necesario que sumen ningún total. Solo puede haber una versión activa del modelo de ponderación a la vez. Para realizar cambios, duplique la versión actual y edite la copia.

![Vista de detalles de un modelo de intención activo](./assets/intent-configuration-model-detail.png){width="550" zoomable="yes"}

Un campo de búsqueda filtra las filas de actividad por nombre. La tabla en sí:

| [!UICONTROL Actividad por intención] | [!UICONTROL IA sugerida] | [!UICONTROL Ponderación] | [!UICONTROL Restablecer] |
| --- | --- | --- | --- |
| Por ejemplo, Agregar a oportunidad, Rellenar formulario, Hacer clic en correo electrónico, Hacer clic en vínculo, Abrir correo electrónico, Cancelar suscripción a un correo electrónico, Visitar página web, Hacer preguntas en un seminario web, Descargas de recursos en un seminario web, Momento interesante, Respondió a la encuesta en un seminario web, Actualizar oportunidad | Solo lectura | Lista desplegable, editable en modelos de borrador | Icono **↺**: restablece esta fila al valor AI sugerido |

**Niveles de ponderación** (la misma escala para las columnas AI sugerida y Ponderación):

| Nivel | Valor |
| ---| --- |
| [!UICONTROL Sin peso] | 0 |
| [!UICONTROL Trivial] | 30 |
| [!UICONTROL Menor] | 40 |
| [!UICONTROL Normal] | 60 |
| [!UICONTROL Importante] | 90 |
| [!UICONTROL Vital] | 100 |

![Cambiando el valor de la actividad Agregar a oportunidad en un modelo de intención de borrador](./assets/intent-configuration-model-edit.png){width="550" zoomable="yes"}

Si se establece una actividad en **[!UICONTROL Sin peso]** (0), se eliminará por completo de la puntuación. El sistema actualmente excluye **[!UICONTROL Cancelar la suscripción al correo electrónico]** de forma predeterminada mediante este método.

Haga clic en **[!UICONTROL Restablecer todo a sugerido]** sobre la tabla para restaurar cada fila a su valor AI sugerido.

### Creación y activación de un modelo

Para crear y activar un nuevo modelo de ponderación, siga estos pasos.

1. Comience desde un modelo _[!UICONTROL Draft]_ existente.

   También puede hacer clic en **[!UICONTROL Duplicar]** para el modelo actual _[!UICONTROL Activo]_ para clonar sus pesos en un nuevo borrador.

1. Ajuste los pesos fila por fila para reflejar lo que importa para su negocio.

   Por ejemplo, rebaja una actividad de señal baja a **[!UICONTROL Trivial]** o actualiza una de señal alta a **[!UICONTROL Importante]** o **[!UICONTROL Vital]**.

1. Haga clic en **[!UICONTROL Guardar]**.

   Al guardar, se le pedirá que active el modelo inmediatamente.

1. Confirme la activación.

La confirmación lo convierte en el nuevo modelo _[!UICONTROL Activo]_ y automáticamente degrada el anterior activo a _[!UICONTROL Archivado]_. Solo puede haber un modelo activo a la vez.

### Columna AI sugerida

La columna Sugerencias de IA es un punto de partida, no una recomendación con formación.

* Una llamada de finalización LLM administra todas las actividades a la vez para un inquilino, no una llamada por actividad.

* Para cada actividad, el modelo solo lee su nombre y descripción y, a continuación, elige un nivel de peso basado en el conocimiento general del comportamiento del comprador B2B. Por ejemplo, considera lo que **[!UICONTROL Rellenar formulario]** o **[!UICONTROL Hacer clic en el correo electrónico]** normalmente indica a un comprador de B2B. No tiene acceso a los datos de cliente, los registros CRM o los patrones de participación históricos del inquilino, y no es específico del inquilino o de la suscripción en la actualidad.

* La salida rellena `SUGGESTED_WEIGHT_VALUE` en `IBG_INTENT_ACTIVITY_WEIGHT` en el momento de la creación del modelo y permanece estática posteriormente. No se actualiza a medida que edita la columna Ponderación.

* Cada fila de actividad siempre tiene un valor sugerido rellenado. Ninguno se deja en blanco.

Revise y ajuste cada fila para reflejar su propio contexto empresarial. Los valores sugeridos son un valor predeterminado razonable, no un modelo ajustado.

## Acciones sobre un modelo

Puede administrar un modelo en función de su estado.

| Acción | Disponible para | ¿Qué sucede? |
| --- | --- | --- |
| **[!UICONTROL Duplicar]** | Activo, Borrador | Abre un modal con el título **[!UICONTROL Duplicate]**, con un campo Name previamente completado y los botones **[!UICONTROL Cancel]** y **[!UICONTROL Duplicate]**. Al confirmar, se crea un nuevo modelo _[!UICONTROL Borrador]_ con los mismos pesos, que se abre directamente en la vista de detalles. |
| **[!UICONTROL Activar]** | Solo borrador (también se ofrece como mensaje justo después de Guardar) | Promociona el borrador a _[!UICONTROL Activo]_ y automáticamente degrada el modelo Activo anterior a _[!UICONTROL Archivado]_. |
| **[!UICONTROL Eliminar]** | Solo borrador | Solicita un cuadro de diálogo de confirmación antes de la eliminación permanente. Esta acción no se puede deshacer. Los modelos activos no se pueden eliminar. |

Como solo los modelos de borrador son editables, el flujo de trabajo normal consiste en hacer clic en **[!UICONTROL Duplicar]** para el modelo _[!UICONTROL Activo]_ actual, ajustar los pesos de la copia de borrador y, a continuación, hacer clic en **[!UICONTROL Guardar]**. Puede activarlo inmediatamente o más tarde con el botón **[!UICONTROL Activar]**.

## Cálculos de ponderación en puntuaciones por intención

La columna **[!UICONTROL Ponderación]** muestra el número usado en la puntuación diaria, leído desde la fila del modelo _[!UICONTROL Activo]_ actual. Tres cosas impulsan la puntuación de la intención de un posible cliente:

1. **El peso configurado aquí** (`WEIGHT_VALUE`) para cada actividad. Comienza con la sugerencia de IA, pero se puede anular por inquilino. Solo se usa la fila vinculada al modelo _[!UICONTROL Active]_, por lo que un cambio de peso no necesita una liberación de código.

1. **Relevancia de contenido**: no se puede configurar aquí. El sistema extrae palabras clave del contenido o los recursos relacionados con la actividad y puntúa la coincidencia de ese contenido con una palabra clave, producto o categoría de 0 a 1.

1. **Frecuencia**: la cantidad de veces que un posible cliente ha interactuado con ese contenido, teniendo en cuenta el promedio de los compromisos de una persona.

Formalmente, por participación: `activity weight × content relevance`, se promedia en una **puntuación diaria** con un declive exponencial de **7 días** aplicado de modo que la actividad reciente domina, luego el mínimo-máximo se normaliza en 0 a 1 en la población actual y se agrupa:

| Puntuación final | Nivel de intención |
| --- | --- |
| > 0.6 | Alto |
| > 0.2 | Medio |
| Caso contrario | Bajo |

### Relevancia de contenido

Para las actividades basadas en la web, el sistema inspecciona la dirección URL del recurso y la compañía asociada y, a continuación, obtiene las palabras clave relevantes de la taxonomía de esa compañía. Por ejemplo, una dirección URL vinculada a [!DNL Intuit] muestra palabras clave como _tax_ o _payroll_. La participación real de un posible cliente con ese contenido (por ejemplo, ver una página de [!DNL TurboTax] o una página de [!DNL QuickBooks]) se compara con esas palabras clave para determinar a qué producto específico se asigna el interés. Para actividades que no son de web, como _[!UICONTROL Momento interesante]_ (incluidos los eventos sin conexión), el modelo evalúa la descripción o el contenido del momento, como un tema de seminario web sin conexión, en lugar del tipo de actividad. El contenido, no la categoría del evento, determina la relevancia.

## Limitaciones conocidas

Las siguientes limitaciones se aplican a la configuración por intención de hoy.

* **Hoy no hay actividades personalizadas o definidas por el inquilino.** El catálogo de actividades es fijo y [!DNL Marketo Engage] es la única fuente fiable. Se debe iniciar sesión en una actividad [!DNL Marketo Engage] para poder clasificarla. Se está creando un ámbito para una columna futura para actividades definidas por el inquilino.
* **No hay ingesta de intención de terceros hoy**, por ejemplo, de [!DNL Demandbase], [!DNL ZoomInfo] o [!DNL 6sense]. Esta actualización está planificada para versiones posteriores. Hasta entonces, la solución consiste en crear la audiencia en la herramienta de terceros e insertarla directamente en [!DNL Marketo Engage] o [!DNL Marketo Optimizer], omitiendo la puntuación por intención para esa señal.
* **No hay exportación nativa** desde el panel de ponderación o desde informes por intención. Consulte [Seguimiento de informes](../agents/intent.md#report-follow-up) para obtener mensajes que conviertan los resultados del informe en una lista de personas.
