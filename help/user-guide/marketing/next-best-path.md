---
title: Siguiente nodo de mejor ruta
description: Obtenga información acerca del nodo de la siguiente mejor ruta de acceso de [!DNL Marketo Optimizer], que usa instrucciones de IA y de lenguaje natural para enrutar los recorridos. Simular rutas antes de publicar.
TQID: 'https://experienceleague.adobe.com/F-pxiABk7vHAktfmBUjZ8BYnxYIwQp--WutG6mvxiY0'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 5229c72e-d79b-574f-a03e-5c4bf48172c3
    internal-label: AI Decisioning
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
    internal-label: Journeys
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 055fd02e1007ba6d06e563dc931adffe6145bed6
workflow-type: tm+mt
source-wordcount: '1556'
ht-degree: 0%
---
# Siguiente nodo de mejor ruta

En [!DNL Marketo Optimizer], el nodo *Siguiente mejor ruta* incorpora la toma de decisiones de ruta dividida impulsada por IA directamente en el lienzo de recorrido. En lugar de configurar las condiciones de filtro en un nodo [rutas divididas](./split-merge-paths-nodes.md), describirá la intención en lenguaje natural y permitirá que el sistema determine la ruta más relevante para cada persona.

En las compras B2B, un perfil puede parecer un tipo de comprador, pero su comportamiento, los datos firmográficos y el contexto de participación revelan una historia con más matices. El siguiente nodo de mejor ruta evalúa ese contexto para tomar una decisión de enrutamiento inteligente, al tiempo que le permite revisar, modificar o anular cualquier recomendación de IA antes de activar el recorrido.

## Path Decisioning {#path-decisioning}

Hay tres pasos para pasar de la intención a la activación.

* **Paso 1: Defina las rutas**: agregue un nodo de la siguiente mejor ruta al recorrido, asigne un nombre a cada ruta y escriba un mensaje en lenguaje natural que describa quién debe avanzar por la ruta. Puede añadir o quitar rutas de acceso en cualquier momento.

* **Paso 2: Simular** — Elija una audiencia de muestra y ejecute una simulación. Verá recuentos de perfiles por ruta, puntuaciones de confianza y el razonamiento de IA para que pueda validar la lógica antes de activarla.

  >[!NOTE]
  >
  >La simulación se ejecuta únicamente con datos de muestra y nunca afecta a la ejecución del recorrido en directo.

* **Paso 3: Activar** — Publica el recorrido en tu audiencia real. La IA evalúa a cada persona en tiempo de ejecución, asigna la ruta que mejor se ajusta en tiempo real y una reserva predeterminada garantiza que nadie se excluya de una ruta.

### Entradas de decisiones de IA {#ai-decisioning-inputs}

Cuando una persona llega al nodo, el sistema obtiene el contexto de perfil, aplica restricciones y utiliza un LLM para seleccionar la ruta que mejor se ajuste. La inteligencia artificial evalúa a cada persona mediante una combinación de las siguientes aportaciones:

* **Historial de participación**: aperturas de correo electrónico, clics en vínculos, visitas a páginas web y otras señales de comportamiento de los recorridos actuales y anteriores
* **Señales en tiempo real**: eventos de alta intención, como rellenos de formularios y visitas a la página de precios
* **Atributos de perfil** - Datos demográficos, de puesto, personales y firmográficos
* **Atributos de cuenta**: datos firmográficos y tecnológicos asociados con la cuenta de la persona

### Creación de contexto de IA {#ai-context-building}

Como apoyo a la decisión de enrutamiento, la IA crea una capa deducida para cada perfil. Combina datos demográficos y firmográficos, detalles de la cuenta y señales de comportamiento (como detalles personales, intención del problema e intención del producto) en un resumen contextual para esa persona. Con este contexto enriquecido, la IA puede dirigir a cada persona hacia el camino óptimo y proporcionar una puntuación de confianza y el razonamiento en lenguaje natural detrás de cada decisión.

Cada decisión se registra con una puntuación de confianza y un razonamiento en lenguaje natural para la transparencia y la observabilidad.

Si ninguna ruta es una coincidencia sólida o si el mensaje hace referencia a datos no disponibles para un perfil, la persona se enruta a la ruta de reserva predeterminada.

## Añadir un siguiente nodo de mejor ruta {#add-node}

1. Abra el recorrido de la persona y vaya al lienzo de recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Siguiente mejor ruta]**.

   ![Menú de opciones de nodo después de hacer clic en el icono de agregar en una ruta de recorrido, con la siguiente mejor ruta de acceso en la lista.](./assets/person-journey-canvas-add-node.png){width="200"}

   El nodo se añade al lienzo y el panel de configuración de la división AI se abre a la derecha. Comienza con una ruta y una ruta predeterminada *Otras personas* para dirigir a las personas que no cumplen los requisitos para ninguna de las rutas definidas.

## Configuración de rutas {#configure-paths}

Para cada ruta, defina un nombre y una petición de datos en lenguaje natural que describa a quién se debe dirigir allí. La entrada del mensaje reemplaza por completo la interfaz de usuario de la condición de filtro; no hay condiciones de atributo que configurar.

1. Para la primera ruta, introduzca las propiedades en la tarjeta de ruta del panel derecho:

   * Escriba una **[!UICONTROL Etiqueta]** que refleje la audiencia o la intención de ese segmento.

   * Escriba un **[!UICONTROL indicador]** en lenguaje natural que describa quién pertenece a esta ruta. Céntrese en la intención y el resultado, no en los valores de atributo específicos.

   ![Tarjeta de ruta de acceso con un campo Etiqueta y un campo Preguntar que describe la audiencia para esa ruta de acceso.](./assets/next-best-path-label-prompt.png){width="500"}

1. Haga clic en **[!UICONTROL Agregar ruta]** para cada ruta adicional que desee incluir.

   Para quitar una ruta, haga clic en el icono *Eliminar* ( ![Eliminar icono](../assets/do-not-localize/icon-delete-2.svg) ) de la tarjeta de ruta.

   Añada la etiqueta y pida confirmación para cada ruta.

   **El ejemplo solicita una división de tres rutas:**

   * *Ruta 1 - Líderes de RRHH:* Identifique a las personas en roles de liderazgo de RRHH que tienen más probabilidades de involucrarse con la administración de talentos y el contenido de experiencia de los empleados.
   * *Ruta 2 - Evaluadores técnicos:* Identifique a las partes interesadas técnicas que tienen más probabilidades de interactuar con la arquitectura del producto, las integraciones y el contenido de implementación.
   * *Ruta 3 - Responsables de la toma de decisiones empresariales:* Identifique a las partes interesadas empresariales que tienen más probabilidades de interactuar con el retorno de la inversión, los resultados empresariales y el contenido de los estudios de casos.

   ![Tres rutas de acceso definidas con indicadores y la ruta de acceso predeterminada Otras personas en el lienzo de recorrido.](./assets/next-best-path-three-defined-paths.png){width="600"}

1. Si es necesario, reordene las rutas para establecer el orden de prioridad de las coincidencias.

   El filtrado de rutas se evalúa en orden descendente. Cada persona continúa por el primer camino que coincida. Haga clic en las flechas arriba y abajo en la parte superior derecha de cada tarjeta de ruta para moverla hacia arriba o hacia abajo en la lista.

1. Revise la ruta predeterminada **[!UICONTROL Otras personas]** (la última de la lista de rutas) y cambie la etiqueta si es necesario.

   La ruta predeterminada se utiliza cuando la IA no puede asignar una persona con seguridad a ninguna ruta definida o cuando los datos relevantes no están disponibles. Cuando una solicitud hace referencia a datos que no existen en el conjunto de datos para un perfil determinado, el sistema enruta ese perfil a la ruta predeterminada e indica el intervalo de datos.

>[!BEGINSHADEBOX]

**Controles humanos en el bucle**

Las recomendaciones de IA no son vinculantes. Antes de activar el recorrido, puede:

* Para restringir la lógica de enrutamiento, edite cualquier solicitud de ruta.
* Agregar, quitar o reordenar rutas.
* Anule las sugerencias de IA con condiciones personalizadas según sea necesario.

Las asignaciones de rutas controladas por IA no surtirán efecto hasta que publique el recorrido.

>[!ENDSHADEBOX]

## Solicitar ejemplos por caso de uso {#prompt-examples}

Los siguientes ejemplos muestran cómo escribir indicadores de ruta efectivos en casos de uso comunes de marketing B2B. Utilícelos como punto de partida y adapte el idioma para que coincida con el contexto de recorrido y los datos de audiencia.

* &quot;Identifique a las personas que han participado en los sitios de RRHH (shrm.org, hbr.org/topic/human-resource-management) y [!DNL Journey Optimizer] durante los últimos 30 días, probablemente para asistir a un seminario web sobre IA en operaciones de RRHH e interesadas en productos de IA&quot;.

* &quot;Identifique a las personas que han participado en sitios de finanzas (wsj.com/finance,investopedia.com), interesadas en [!DNL Marketo Engage] en los últimos 30 días y que probablemente asistan a un seminario web sobre IA en Financial Planning. También deberían haber mostrado cierto interés en los productos de IA&quot;.

* &quot;Identifique a las personas que participaron en los sitios de Riesgo/Investigación (mckinsey.com/capabilities/risk-and-resilience, forrester.com/research) y [!DNL GenStudio] en los últimos 30 días, probablemente para asistir a un seminario web sobre IA en Gestión de Riesgos e interesadas en los productos de IA&quot;.

## Simular la toma de decisiones antes de publicar {#simulate}

Utilice la simulación para probar cómo la IA evalúa los indicadores con respecto a una audiencia real antes de que el recorrido se active. La simulación solo está disponible mientras el recorrido esté en estado *Borrador* y no tiene efecto en ningún recorrido publicado.

### Ejecución de una simulación {#run-simulation}

1. Seleccione el siguiente nodo de mejor ruta y haga clic en el icono *Simular* ( ![Icono Simular](../assets/do-not-localize/icon-simulate.svg) ) en la parte superior del panel derecho.

1. En el cuadro de diálogo, elija una lista dinámica para utilizarla en la audiencia de simulación.

<!-- 
   * **[!UICONTROL Original person lists]** – Use the audience from the audience node. Specify a sample size when the full audience exceeds the simulation threshold.
   * **[!UICONTROL Dynamic and static lists]** – Use a [!DNL Marketo Engage] static or dynamic list.
   * **[!UICONTROL Test records]** – Use AI-suggested test profiles.
-->

![Simular diálogo de rutas de acceso con una lista dinámica seleccionada y los botones Cancelar y Simular.](./assets/next-best-path-simulate-paths.png){width="250"}

>[!NOTE]
>
>* Si la audiencia seleccionada supera el umbral de simulación, el sistema ejecuta la simulación en una muestra de 100 perfiles. Un indicador en la IU muestra que los resultados se basan en muestras.
>* Si la audiencia seleccionada aún no se ha materializado, la simulación se bloquea. Una advertencia en línea le indica que primero debe materializar la audiencia.

1. Haga clic en **[!UICONTROL Simular]**.

### Revisar resultados de simulación {#review-results}

Después de ejecutar la simulación, el panel derecho muestra la distribución de perfiles en cada ruta y el razonamiento de IA detrás de esas asignaciones:

| Resultado | Descripción |
|---|---|
| **Perfiles** | El número de perfiles enrutados a la ruta. |
| **División** | El porcentaje de perfiles enrutados a la ruta. |
| **Confianza** | Nivel de confianza de IA para la asignación de ruta. La confianza refleja la actualización de los datos, la intensidad y la coherencia de la señal y el éxito histórico de patrones de enrutamiento similares. |
| **Mensaje** | El indicador que se evaluó para la ruta. |
| **Razonamiento de IA** | Una explicación en lenguaje natural de por qué los perfiles se asignaron colectivamente a esta ruta. |

![Resultados de simulación que muestran el recuento de perfiles, el porcentaje dividido, la puntuación de confianza y el razonamiento de IA por ruta.](./assets/next-best-path-simulated-details.png){width="600"}

>[!NOTE]
>
>Cuando los datos disponibles o el alcance limitan una decisión, los resultados incluyen información sobre la limitación. Por ejemplo, cuando un atributo requerido no está presente en el conjunto de datos, los resultados incluyen un indicador explícito que explica cómo los datos que faltan afectaron a los resultados.

Utilice los resultados para restringir las peticiones de datos y confirmar que la ruta refleja el resultado deseado. Puede modificar los indicadores de ruta y volver a ejecutar la simulación tantas veces como sea necesario antes de publicar.

## Publicación y monitorización del recorrido {#publish-monitor}

Después de validar los resultados de la simulación:

1. Conecte la audiencia de personas al nodo de entrada de recorrido.

1. [Publicación del recorrido](./person-journeys.md#publish).

Una vez que el recorrido está activo, el siguiente nodo de mejor ruta se ejecuta en el momento de la ejecución. A medida que cada persona llega al nodo, la IA los evalúa en tiempo real utilizando las señales más recientes y los enruta hacia la ruta más relevante.

Para un recorrido publicado, abra el lienzo de recorrido y seleccione el siguiente nodo de mejor ruta para ver la sección **_[!UICONTROL Resultados finales]_** en el panel derecho. Los resultados finales muestran:

* La distribución porcentual de perfiles en cada ruta
* La puntuación de confianza para cada asignación de ruta
* Razonamiento a nivel de ruta y de perfil, con detalles ampliables para perfiles individuales

![Pestaña de informe final que muestra la distribución del perfil en directo, las puntuaciones de confianza y el razonamiento de IA por ruta.](./assets/next-best-path-final-report.png){width="600"}

Los resultados en vivo también están disponibles a través de la habilidad Observabilidad del Recorrido en la [interfaz de chat de Coworker](../agents/chat-interface.md).
