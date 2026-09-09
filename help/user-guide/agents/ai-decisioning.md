---
title: AI Decisioning
description: Comprenda la toma de decisiones de IA en Marketo Optimizer, la capa de inteligencia detrás del control de tráfico de recorrido, la siguiente mejor ruta, la optimización del tiempo de envío y otras funcionalidades que reemplazan las reglas estáticas con la automatización basada en resultados.
TQID: 'https://experienceleague.adobe.com/biPd2Zv3z75i7imGqRNuKXvgoD0sIcwrFrjWmSO7FpU'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2:
  - id: 3cf5f37e-e87e-5179-812b-53ce05d7eebb
  - id: 5229c72e-d79b-574f-a03e-5c4bf48172c3
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 808
ht-degree: 2%

---


# decisiones de IA

La toma de decisiones de IA es la capa de inteligencia detrás de Adobe Marketo Optimizer. En lugar de crear previamente cada rama como regla estática, AI Decisioning evalúa continuamente el contexto de un perfil, incluida la pertenencia al recorrido, el historial de participación, las puntuaciones de intención y la conducta en tiempo real, para determinar la siguiente mejor acción o ruta para esa persona.

Esta evaluación continua mueve la orquestación de las reglas estáticas a la automatización impulsada por resultados: en lugar de definir cada condición por adelantado, se describe el resultado que se desea y el sistema determina cómo llegar allí para cada persona.

## Competencias {#capabilities}

La toma de decisiones de IA se compone de las siguientes capacidades:

| Capacidad | Lo que decide |
|---|---|
| [control de tráfico de Recorrido](../marketing/journey-traffic-control.md) | En qué recorrido debería estar una persona en este momento. Cuando una persona cumple los requisitos para más de un recorrido, el control de tráfico de recorrido los redirige en el momento en que cambia su perfil o conducta, en lugar de dejarlos en un camino que ya no encaja. |
| [Siguiente mejor ruta](../marketing/next-best-path.md) | La ruta más adecuada para una persona dentro de un recorrido. En lugar de codificar las condiciones de filtro, se describe la intención en lenguaje natural, y el sistema enruta a cada persona a la ruta que mejor coincida en el momento adecuado. |
| [Optimización del tiempo de envío](../marketing/email-send-time-optimization.md) | La mejor ventana de envío para cada destinatario, en función de la participación histórica, en lugar de una programación fija para todos. |
| Contenido contextual | Variantes de correo electrónico personalizadas generadas automáticamente a partir de una información breve de contenido, para usarlas como un único recurso de correo electrónico personalizado dentro de recorrido. _Próximamente._ |
| [Brand Concierge](https://experienceleague.adobe.com/es/docs/brand-concierge/content/home){target="_blank"} | Enrutamiento y respuesta conversacional en tiempo real, como chat y asistencia en vivo. Brand Concierge requiere derechos de producto adicionales. |

Algunas de estas funcionalidades solucionan diferentes problemas dentro del mismo recorrido. El control de tráfico de recorrido decide qué recorrido gana la prioridad cuando varios recorridos compiten para atraer a la misma persona al mismo tiempo. Las otras capacidades deciden qué sucede después de que una persona ya está en un recorrido.

## Dividir rutas y la siguiente mejor ruta {#split-paths-next-best-path}

[Las rutas divididas](../marketing/split-merge-paths-nodes.md) le permiten definir ramas de recorrido con condiciones de filtro explícitas: si una puntuación está por encima de un umbral, envíe a una persona por una ruta o, en caso contrario, envíe a otra. Esta lógica basada en reglas es precisa y totalmente auditable, pero cada nueva condición requiere una nueva rama.

El nodo [Siguiente mejor ruta](../marketing/next-best-path.md) aplica la toma de decisiones de IA al mismo problema. En lugar de un umbral fijo, el modelo evalúa la participación, el perfil, el interés del producto y la fase de funnel juntos, predice el mejor resultado para cada persona y selecciona la ruta óptima automáticamente.

## Entradas de datos {#data-inputs}

La toma de decisiones de IA se basa en las siguientes categorías de datos:

| Categoría | Ejemplos |
|---|---|
| Demográfico y firmográfico | Cargo, sector y tamaño de la empresa |
| Psicográfico | Puntuación, urgencia y prioridad de posibles clientes |
| Participación | Puntuación, nivel, tendencia, última actividad y canal |
| Intención | Intento de producto o palabra clave, agrupados en bloques altos, medios o bajos |
| Persona | Función en el trato, el cargo y la personalidad |

## Cadencia de evaluación {#evaluation-cadence}

La toma de decisiones de IA utiliza dos horarios de evaluación diferentes. El perfil subyacente de una persona se vuelve a calcular en un lote nocturno. La decisión en sí se aplica en tiempo real en cada interacción, utilizando lo que indique el perfil nocturno más reciente. Por lo tanto, la parte continua de la toma de decisiones de IA describe el momento de la decisión, no la velocidad de actualización del perfil.

## Protecciones y reglas {#guardrails-rules}

Las reglas solo cubren condiciones que alguien escribió explícitamente. Cuando la realidad cae fuera de ese árbol, como una personalidad híbrida o una combinación de señales que nadie anticipó, las reglas no hacen nada hasta que alguien agrega una nueva rama. La toma de decisiones de IA puntúa a cada persona continuamente y genera una mejor acción basada en la confianza en su lugar, por lo que gestiona combinaciones para las que nadie está programado explícitamente, y mejora a medida que ve más resultados, lo que una regla nunca hace.

Las reglas son explicables e instantáneas para la auditoría, mientras que la toma de decisiones de IA tiene una puntuación de confianza en lugar de ser determinista. Por esta razón, las reglas siguen siendo la mejor herramienta cuando:

* Nunca se debe cruzar un límite de cumplimiento estricto, como suprimir los contactos de exclusión.
* No hay suficiente volumen o historial para que un modelo aprenda todavía.
* Cada decisión debe ser plenamente explicable cuando se solicite.

La mayoría de las configuraciones maduras funcionan ambas juntas: reglas como protecciones y decisiones de IA que administran todo lo que hay entre medias.

## Ventajas {#benefits}

* Menos complejidad de recorrido manual, con menos ramas de reglas que mantener.
* Experiencias más relevantes sin construir cientos de reglas.
* Mayor eficiencia en la calificación.
* Identificación más rápida de la siguiente mejor participación para cada perfil.

>[!BEGINSHADEBOX]

**Ámbito futuro: contexto de cuenta y grupo de compra**

No disponible hoy en Marketo Optimizer. La toma de decisiones de IA está planificada para extenderse más allá del perfil individual a:

* Contexto de cuenta: las señales a nivel de compañía y cuenta como entrada de toma de decisiones.
* Señales de grupo de compra: función en el acuerdo, estado del responsable de la toma de decisiones o del profesional y participación acumulada en todos los participantes en una decisión de compra.
* Organización de recorridos a nivel de cuenta: decisiones de enrutamiento y contenido tomadas para la cuenta o el grupo de compra como unidad, con control de tráfico de recorrido coordinado entre las distintas personas involucradas.

>[!ENDSHADEBOX]
