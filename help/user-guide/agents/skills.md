---
title: Aptitudes de compañeros
description: 'Revise las habilidades de los compañeros de CX Enterprise en Marketo Optimizer: flujos de trabajo empaquetados para programas, recorridos, audiencias, puntuación, contenido y optimización del tiempo de envío.'
TQID: 'https://experienceleague.adobe.com/nNFB9UEghfqVvnBrNtTDnpnLUKKKMAU2nY1Pqt0KkUQ'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2:
  - id: 3cf5f37e-e87e-5179-812b-53ce05d7eebb
  - id: 46e599c6-e20f-5f67-9824-93415016f66b
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
  - id: a29661b8-f7a4-53d1-a9ac-fdec08c092e4
  - id: d4203578-d294-5145-b397-f26f4488a904
topic_v2:
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 581
ht-degree: 7%

---

# Aptitudes de compañero

Una _aptitud_ es un flujo de trabajo empaquetado que el Compañero de trabajo sabe cómo ejecutar: los componentes básicos detrás del menú `/` y de las solicitudes en lenguaje natural. Cada aptitud agrupa instrucciones paso a paso y las herramientas específicas necesarias para un trabajo (por ejemplo, &quot;publicar un recorrido&quot;, &quot;comparar dos listas de personas&quot;, &quot;crear un modelo de puntuación&quot;).

>[!NOTE]
>
>Cada aptitud se clasifica de acuerdo con si la aptitud muta el estado [!DNL Marketo Optimizer] o [!DNL Marketo Engage] (**Write**), solo genera/analiza (**Read**) o si tiene funciones de consulta y mutación de igual a igual (**Read+Write**).

## Programas y planificación {#programs-planning}

| Habilidad | Qué hace | Acceso | Superficie del producto | Impacto / Flujo de datos |
|---|---|---|---|---|
| `falco-program-creation` | Creación de programas de [!DNL Marketo Optimizer] de extremo a extremo: programas, subcarpetas, tokens, listas y recorridos. <p>Ver _[Crear un programa a partir de una breve](./program-from-brief.md)_. | Escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer]. |
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
| `journey-observability` | Depuración/monitorización de la progresión: rutas, tiempo, divisiones, paradas, permanencia. <p>Ver _[Depurar y supervisar la progresión del recorrido](./journey-observability.md)_. | Lectura | [!DNL Marketo Optimizer] | Lee [!DNL Marketo Optimizer] + [!DNL Marketo Engage] (comprobación de lista estática) |

## Audiencias y personas {#audiences-people}

| Habilidad | Qué hace | Acceso | Producto | Back-end (flujo de datos) |
|---|---|---|---|---|
| `audience-creation` | Adaptar una lista inteligente [!DNL Marketo Engage], crear una lista de personas o agregar o actualizar reglas. <p>Ver _[Crear audiencias para programas](./audience-creation.md)_. | Escritura | [!DNL Marketo Optimizer] | Lee [!DNL Marketo Engage] + lee/escribe [!DNL Marketo Optimizer]. |
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
| `scoring-studio` | Enumere u obtenga modelos de puntuación y créelos o publíquelos. <p>Ver _[Crear modelos de puntuación personalizados](./lead-scoring-model.md)_. | Lectura y escritura | [!DNL Marketo Optimizer] | Lee y escribe [!DNL Marketo Optimizer] (servicio de puntuación); lee [!DNL Marketo Engage] campos de posible cliente/tipos de actividad. |
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
