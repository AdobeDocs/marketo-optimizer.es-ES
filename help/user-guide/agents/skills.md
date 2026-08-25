---
title: Aptitudes de compañeros
description: 'Revise las aptitudes de los compañeros en Marketo Optimizer: flujos de trabajo empaquetados para programas, recorridos, audiencias, puntuación, contenido y optimización del tiempo de envío.'
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 7%

---

# Aptitudes de compañero

Una _aptitud_ es un flujo de trabajo empaquetado que el agente sabe cómo ejecutar: los componentes básicos del menú `/` y de las solicitudes en lenguaje natural. Cada aptitud agrupa instrucciones paso a paso y las herramientas específicas necesarias para un trabajo (por ejemplo, &quot;publicar un recorrido&quot;, &quot;comparar dos listas de personas&quot;, &quot;crear un modelo de puntuación&quot;).

>[!NOTE]
>
>Cada aptitud se clasifica de acuerdo con si la aptitud muta el estado [!DNL Marketo Optimizer] o [!DNL Marketo Engage] (**Write**), solo genera/analiza (**Read**) o si tiene funciones de consulta y mutación de igual a igual (**Read+Write**).

## Programas y planificación {#programs-planning}

| Habilidad | Qué hace | Acceso | Superficie del producto | Impacto / Flujo de datos |
|---|---|---|---|---|
| `falco-program-creation` | Creación de programas de [!DNL Marketo Optimizer] de extremo a extremo: programas, subcarpetas, tokens, listas y recorridos. | Escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer]. Ver _[Crear un programa a partir de una breve](./program-from-brief.md)_. |
| `adapt-program` | Generar historias de migración de [!DNL Marketo Engage] programas para la adaptación [!DNL Marketo Optimizer]. | Lectura | [!DNL Marketo Optimizer] | Lee [!DNL Marketo Engage], escribe [!DNL Marketo Optimizer] |
| `folder-creation` | Cree carpetas organizativas en el árbol de recursos. | Escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer] |
| `program-creation` *(Programas de compilación)* | Cree programas de Marketo a partir de una información de campaña. | Escritura | [!DNL Marketo Engage] | Lee y escribe [!DNL Marketo Engage] |
| `program-planning` *(Planificar campañas)* | Transforme informes en documentos de configuración/implementación. | Lectura | [!DNL Marketo Engage] | Lee [!DNL Marketo Engage] |
| `program-qa` *(Validar programas)* | Validar/auditar programas (solo reglas, plan de prueba o resumen). | Lectura | [!DNL Marketo Engage] | Lee [!DNL Marketo Engage] |

## Recorridos {#journeys}

| Habilidad | Qué hace | Acceso | Producto | Back-end (flujo de datos) |
|---|---|---|---|---|
| `journey-creation` | Cree y edite recorridos de persona a partir del lenguaje natural. | Escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer] |
| `journey-edit-dates` | Cambiar la fecha de inicio o finalización de un recorrido sin publicarlo. | Escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer] |
| `journey-publish` | Publicar/iniciar/programar recorridos de personas. | Escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer] |
| `journey-stop` | Abortar, cerrar, parar, detener o matar recorridos. | Escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer] |
| `journey-reentry` | Configurar la reentrada: permitir/no permitir, reutilización, máximo de entradas. | Escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer] |
| `journey-trafficcontrol` | Ejecute una simulación de control de tráfico que muestre el enrutamiento de perfiles. | Lectura | [!DNL Marketo Optimizer] | Lee [!DNL Marketo Optimizer] (simulación) |
| `journey-observability` | Depuración/monitorización de la progresión: rutas, tiempo, divisiones, paradas, permanencia. | Lectura | [!DNL Marketo Optimizer] | Lee [!DNL Marketo Optimizer] + [!DNL Marketo Engage] (comprobación de lista estática) |

## Audiencias y personas {#audiences-people}

| Habilidad | Qué hace | Acceso | Producto | Back-end (flujo de datos) |
|---|---|---|---|---|
| `audience-creation` | Adaptar una lista inteligente [!DNL Marketo Engage], crear una lista de personas o agregar o actualizar reglas. | Escritura | [!DNL Marketo Optimizer] | Lee [!DNL Marketo Engage] + lee/escribe [!DNL Marketo Optimizer].  Ver _[Crear audiencias para programas](./audience-creation.md)_. |
| `people-list-comparison` | Comparar listas de dos personas y mostrar miembros superpuestos. | Lectura | [!DNL Marketo Optimizer] | Lee [!DNL Marketo Optimizer] |
| `import-leads` | Inspeccionar la calidad de los datos CSV y confirmar las importaciones en [!DNL Marketo Engage]. | Lectura y escritura | Ambos | Lee y escribe [!DNL Marketo Engage] |
| `lead-investigation` *(investigar posibles clientes)* | Investigue la actividad, puntuación, calificación y ciclo de vida de un posible cliente. | Lectura | [!DNL Marketo Engage] | Lee [!DNL Marketo Engage] |

## Contenido y canales {#content-channels}

| Habilidad | Qué hace | Acceso | Producto | Back-end (flujo de datos) |
|---|---|---|---|---|
| `content-personalization` | Examinar/previsualizar plantillas y editar contenido/generar variantes. | Lectura y escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer]. Ver _[Personalizar contenido de correo electrónico por persona](./personalize-content.md)_. |
| `asset-tokens` | Token completo CRUD en programas/carpetas/recorridos. | Lectura y escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer] |
| `fcs-channels` | Búsquedas de canal y CRUD + publicar/detener/eliminar. | Lectura y escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer] |

## Puntuación y señales {#scoring-signals}

| Habilidad | Qué hace | Acceso | Producto | Back-end (flujo de datos) |
|---|---|---|---|---|
| `scoring-studio` | Enumere u obtenga modelos de puntuación y créelos o publíquelos. | Lectura y escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer] (servicio de puntuación); lee [!DNL Marketo Engage] campos de posible cliente/tipos de actividad. Ver _[Crear modelos de puntuación personalizados](./lead-scoring-model.md)_. |
| `engagementconfiguration` | Mostrar configuración de participación y editar/actualizar ponderaciones. | Lectura y escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer] |
| `intentconfiguration` | Mostrar configuración por intención y establecer/actualizar pesos. | Lectura y escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer] |
| `intent-query` | Consultar y explicar las puntuaciones por intención por persona/segmento/lista. | Lectura | [!DNL Marketo Optimizer] | Lee [!DNL Marketo Optimizer] |

## Optimización del tiempo de envío {#sto}

| Habilidad | Qué hace | Acceso | Producto | Back-end (flujo de datos) |
|---|---|---|---|---|
| `send-time-optimization` | Compruebe el estado de STO y habilite/deshabilite en un nodo de correo electrónico. | Lectura y escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer] |
| `send-time-report` | Buscar/mostrar el informe de rendimiento de STO. | Lectura | [!DNL Marketo Optimizer] | Lee [!DNL Marketo Optimizer] |

## Conocimiento {#knowledge}

| Habilidad | Qué hace | Acceso | Producto | Back-end (flujo de datos) |
|---|---|---|---|---|
| `product-knowledge` | Responda preguntas sobre procedimientos y conceptos a partir de la documentación de [!DNL Marketo Optimizer] en Experience League. | Lectura | Ambos | Lee documentos externos sin datos del producto |

## Cross-back-end {#cross-backend}

Estas aptitudes abarcan más de un servidor:

- **`adapt-program`** — `gather_program_assets` lee [!DNL Marketo Engage] (`get_program`, `get_smart_campaign`, `list_emails`) y luego escribe a través de `falcomcp_create_journey` — backend clásico.
- **`audience-creation`** — lee [!DNL Marketo Engage] listas inteligentes (`get_smart_list` / `get_smart_campaign`) y luego escribe [!DNL Marketo Optimizer] listas de personas.
- **`journey-observability`** — [!DNL Marketo Optimizer] lecturas más `check_lead_in_marketo_static_list` [!DNL Marketo Engage] lecturas.
- **`scoring-studio`** — lee [!DNL Marketo Engage] campos de posible cliente/tipos de actividad junto con el servicio de puntuación [!DNL Marketo Optimizer].

Todas las herramientas `falco-mcp_*` y recorrido/token/puntuación/STO/FCS llegan a [!DNL Marketo Optimizer] servicios; CSV/programa/herramientas de posible cliente llegan a [!DNL Marketo Engage].

