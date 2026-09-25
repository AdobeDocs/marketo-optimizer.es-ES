---
title: Aptitudes de compañeros
description: Revise las habilidades de los compañeros de trabajo en Marketo Optimizer para recorridos, audiencias, programas, contenido, análisis y toma de decisiones de IA. Aprenda lo que cada aptitud puede hacer por usted.
autotag-review: '2026-09-22T14:02:17.516Z'
TQID: 'https://experienceleague.adobe.com/nNFB9UEghfqVvnBrNtTDnpnLUKKKMAU2nY1Pqt0KkUQ'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 1650dadf-b034-5ac9-a309-77ad1e2f5035
    internal-label: Chat Interface
subfeature_v2:
  - id: b9e5c7f3-be30-563c-9e41-cc8ea76e2fee
    internal-label: Skills
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
source-git-commit: 5334f0f5d9d958ea47b055b067a7308950352e9c
workflow-type: tm+mt
source-wordcount: '988'
ht-degree: 4%
---

# Aptitudes de compañero

Una _aptitud_ es un flujo de trabajo empaquetado que el Compañero de trabajo puede ejecutar. Las habilidades son los componentes detrás del menú `/` y de las solicitudes en lenguaje natural. Cada aptitud agrupa instrucciones paso a paso y las herramientas específicas necesarias para una tarea, como publicar un recorrido, comparar listas de dos personas o crear un modelo de puntuación.

La clasificación de cada aptitud refleja el tipo de acción que realiza:

* _Buscar_ aptitudes busca o enumera registros existentes.
* _Analizar_ habilidades para revisar, comparar o generar informes sobre datos sin cambiarlos.
* _Ver_ aptitudes muestran un informe o una métrica de solo lectura.
* _Editar_ aptitudes cambia la configuración o el contenido de un objeto existente.
* _Crear_ aptitudes para crear un nuevo objeto.

## Recorridos {#journeys}

Estas habilidades crean, publican, depuran y administran recorridos de personas.

| Habilidad | Qué hace | Tipo |
| --- | --- | --- |
| **Observabilidad del Recorrido** | Depure y supervise el movimiento de personas a través de un recorrido, incluidas las rutas, el tiempo de espera, las divisiones, los puestos y el tiempo de permanencia. Ver _[Depurar y supervisar la progresión del recorrido](./journey-observability.md)_. | Analizar |
| **Control de tráfico de Recorrido** | Simule cómo se distribuyen los perfiles en todos los recorridos activos. | Analizar |
| **Publicación de Recorrido** | Publicar, iniciar o programar un recorrido, incluido el modo de inicio, las fechas y la confirmación. | Editar |
| **Detención de Recorrido** | Interrumpa un recorrido en marcha para detenerlo inmediatamente o ciérrelo para bajarlo correctamente. | Editar |
| **Fechas de edición de Recorrido** | Cambie la fecha de inicio o finalización en un recorrido en borrador, programado o activo sin volver a publicarlo. | Editar |
| **Reentrada de Recorrido** | Configure los ajustes de reentrada para un recorrido, incluyendo si se permite la reentrada, el retraso de reutilización y el recuento máximo de entradas. | Editar |
| **Creación de Recorrido** | Cree y edite recorridos de persona mediante solicitudes en lenguaje natural. | Crear |
| **Seminario web al Recorrido** | Configure un recorrido promocional antes de un seminario web y un recorrido de seguimiento después. | Crear |

## Listas de audiencia y personas {#audience-people-lists}

Estas habilidades crean y administran listas de personas y definiciones de audiencias.

| Habilidad | Qué hace | Tipo |
| --- | --- | --- |
| **Examinar miembros de lista dinámica** | Examine y filtre los miembros de una lista de personas dinámica o estática. | Buscar |
| **Comparación de listas de personas** | Comparar listas de dos personas y mostrar miembros superpuestos. | Analizar |
| **Quitar de la lista estática** | Quite los miembros que coincidan con los criterios de lenguaje natural de una lista estática. | Editar |
| **Creación de audiencias** | Adaptar una lista inteligente [!DNL Marketo Engage], crear una lista de personas o agregar o actualizar sus reglas. Ver _[Crear audiencias para programas](./audience-creation.md)_. | Crear |

## Programas, carpetas y canales {#programs-folders-channels}

Estas habilidades administran la estructura del programa, los tokens y la configuración del canal.

| Habilidad | Qué hace | Tipo |
| --- | --- | --- |
| **Crear programa** | Cree programas a partir de una información de campaña. Ver _[Crear un programa a partir de una breve](./program-from-brief.md)_. | Analizar |
| **Programa de adaptación** | Generar historias de migración de [!DNL Marketo Engage] programas para la adaptación [!DNL Marketo Optimizer]. | Analizar |
| **Tokens de recursos** | Crear y administrar valores de `{{my.token}}` en programas, carpetas y recorridos. | Editar |
| **Canales FCS** | Cree, publique, detenga y clone canales en el servicio de canales, incluidos los esquemas XDM y el aprovisionamiento. | Editar |
| **Creación de carpeta** | Cree carpetas organizativas en el árbol de recursos. | Crear |
| **Campaña en línea WhatsApp** | Cree y publique una campaña en línea de [!DNL WhatsApp] en un nodo de recorrido. | Crear |
| **Creación de programas de mercadotecnia** | Cree un programa completo que incluya subcarpetas, tokens, listas de personas y recorridos. | Crear |
| **Creación de lotes de programas y Recorridos** | Cree varios pares de programa y recorrido en una única solicitud por lotes. | Crear |

## Correo electrónico y páginas de aterrizaje {#email-landing-pages}

Estas habilidades crean y administran correos electrónicos, formularios y páginas de aterrizaje.

| Habilidad | Qué hace | Tipo |
| --- | --- | --- |
| **Lista de Forms** | Enumerar formularios y ver sus detalles y campos. | Buscar |
| **Páginas de aterrizaje de lista** | Enumere las páginas de aterrizaje, vea sus detalles y administre su estado de borrador o publicado. | Buscar |
| **Auditoría de correo electrónico** | Auditar un correo electrónico en relación con su grupo de destino, incluida la inferencia personal y una breve revisión sección por sección. | Analizar |
| **Creación de correo electrónico** | Cree o actualice un nodo de correo electrónico de recorrido, incluyendo la composición a partir de un informe o PDF, su vinculación a un nodo y la escritura de contenido. | Editar |
| **Creación de formularios** | Cree o actualice un formulario independiente de captura de posibles clientes, publíquelo y, opcionalmente, incrústelo en una página de aterrizaje. | Crear |
| **Creación de páginas de aterrizaje** | Cree o actualice una página de aterrizaje a partir de un informe, incluida la planificación de contenido, la selección de plantillas, el rellenado de espacios y la adición de un formulario; a continuación, publíquelo. Adjunte también una página de aterrizaje publicada como vínculo de call-to-action en un correo electrónico. | Crear |
| **Comprobación de procesamiento de correo electrónico** | Busque en un correo electrónico [!DNL Microsoft Outlook] problemas de procesamiento y corrija automáticamente lo que puede hacer. | Editar |

## Personalización de contenido {#content-personalization}

Esta aptitud explora plantillas y personaliza el contenido del correo electrónico para diferentes personalidades.

| Habilidad | Qué hace | Tipo |
| --- | --- | --- |
| **Personalization de contenido** | Examine y previsualice las plantillas y, a continuación, edite el contenido o genere variantes. Ver _[Personalizar contenido de correo electrónico por persona](./personalize-content.md)_. | Crear |

## Analytics y optimización {#analytics-optimization}

Estas habilidades informan sobre el rendimiento y configuran la optimización del tiempo de envío y los modelos de puntuación.

| Habilidad | Qué hace | Tipo |
| --- | --- | --- |
| **Surface Analytics** | Genere informes de análisis a partir de solicitudes en lenguaje natural, que cubran las tendencias de actividad, el rendimiento de los correos electrónicos, los datos de clientes potenciales y cuentas, la pertenencia a segmentos y listas y las métricas de recorridos. Los datos del informe se actualizan cada dos horas. Consulte _[Generar informes de análisis](./surface-analytics.md)_. | Analizar |
| **Informe de tiempo de envío** | Vea el informe de rendimiento de la optimización del tiempo de envío (STO) en el nivel de recorrido o para un nodo de correo electrónico individual. | Analizar |
| **Simulación STO de correo electrónico** | Previsualice el tiempo de envío previsto, la calidad de audiencia y el mapa de calor de participación de un nodo de correo electrónico antes de habilitar STO. | Analizar |
| **Optimización del tiempo de envío** | Habilite o deshabilite STO en un nodo de correo electrónico de recorrido. | Editar |
| **Configuración de participación** | Muestre y edite las ponderaciones de actividad del modelo de puntuación de participación de la persona. | Editar |
| **Estudio de puntuación** | Enumere y vea modelos de puntuación y, a continuación, cree y publique otros nuevos. Ver _[Crear modelos de puntuación personalizados](./lead-scoring-model.md)_. | Crear |

## Toma de decisiones e intención de IA {#ai-decisioning-intent}

Estas habilidades evalúan la preparación de los datos para la toma de decisiones de IA y configuran la puntuación por intención.

| Habilidad | Qué hace | Tipo |
| --- | --- | --- |
| **Estado de decisiones de IA** | Informe de si los datos de una organización están listos para la toma de decisiones de IA, incluida la disponibilidad de posibles clientes, la distribución personal, la riqueza de historias y la intención. | Analizar |
| **Analizar intención** | Consulte y valide la clasificación por intención en el nivel de posible cliente, las tendencias y la taxonomía de productos y palabras clave. | Analizar |
| **Configuración por intención** | Muestre y edite las ponderaciones de actividad del modelo de puntuación por intención de persona. | Editar |

## Gestión de conocimientos y aptitudes {#knowledge-skill-management}

Estas habilidades responden a preguntas sobre productos y le permiten crear nuevas habilidades personalizadas.

| Habilidad | Qué hace | Tipo |
| --- | --- | --- |
| **Conocimiento del producto** | Responda preguntas conceptuales y de procedimientos utilizando la documentación de [!DNL Marketo Optimizer] publicada en Experience League. | Buscar |
| **Creación de habilidades** | Cree, pruebe y perfeccione nuevas habilidades personalizadas. | Crear |
