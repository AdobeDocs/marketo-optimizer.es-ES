---
title: Información general sobre CX Enterprise Coworker en Adobe Marketo Optimizer
description: Descubra cómo CX Enterprise Coworker utiliza las habilidades de Marketo Optimizer para crear y adaptar programas, comprobar la preparación para la toma de decisiones de IA y llamar a las herramientas de MCP.
autotag-review: '2026-11-24T22:43:00.917Z'
TQID: https://experienceleague.adobe.com/V4Kww-NcdfbFxXqWrs7mPq7UYu8AREqDgyfvlMnlURM
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 1650dadf-b034-5ac9-a309-77ad1e2f5035
    internal-label: Chat Interface
  - id: 5229c72e-d79b-574f-a03e-5c4bf48172c3
    internal-label: AI Decisioning
  - id: a29661b8-f7a4-53d1-a9ac-fdec08c092e4
    internal-label: Programs
subfeature_v2:
  - id: b9e5c7f3-be30-563c-9e41-cc8ea76e2fee
    internal-label: Skills
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
source-git-commit: 418b81a0a39eca0ca7b537c76da972df7eefd09f
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 2%
---

# [!DNL CX Enterprise Coworker] en [!DNL Adobe Marketo Optimizer] {#coworker-overview}

El chat de [!DNL CX Enterprise Coworker] es una interfaz conversacional para completar tareas en [!DNL Adobe Marketo Optimizer]. Describa una meta en lenguaje sencillo y [!DNL Coworker] planificará las tareas, las ejecutará en [!DNL Marketo Optimizer], validará los resultados y proporcionará el trabajo terminado para su aprobación.

[!DNL Coworker] usa habilidades creadas para [!DNL Marketo Optimizer] para guiarle a través de tareas de operaciones de marketing comunes: crear un nuevo programa, adaptar un programa de [!DNL Marketo Engage] existente y comprobar si los datos están listos para la toma de decisiones de IA.

[!DNL Coworker] respeta los [[!DNL Marketo Optimizer] permisos](../start/permissions-reference.md) existentes de su organización. Solo puede realizar las acciones que ya tiene permiso para realizar y los administradores controlan cuándo tiene acceso de escritura. [!DNL Coworker] forma parte del ecosistema de Adobe y no se limita a [!DNL Marketo Optimizer].

Para obtener más información, consulte:

* [Resumen de chat de [!DNL Adobe CX Enterprise Coworker]](https://experienceleague.adobe.com/es/docs/coworker/content/chat/overview)
* [Interfaz de chat en  [!DNL Marketo Optimizer]](./chat-interface.md)
* [[!DNL Coworker] aptitudes en  [!DNL Marketo Optimizer]](./skills.md)

## [!DNL Marketo Optimizer] aptitudes en [!DNL CX Enterprise Coworker] {#skills}

Utilice las siguientes habilidades específicas del producto para crear y adaptar programas o evaluar la preparación de los datos.

| Habilidad | Lo que le ayuda a hacer | Solicitud de ejemplo |
| --- | --- | --- |
| `program-creation-marketo-optimizer` | Crear un programa de marketing [!DNL Marketo Optimizer] de principio a fin. [!DNL Coworker] le guía desde su objetivo hasta un programa creado. | Cargue un informe de campaña y, a continuación, pregunte: _Cree un programa con el informe adjunto._ |
| `adapt-program-marketo-optimizer` | Adaptar, migrar o convertir un programa [!DNL Marketo Engage] existente en un programa [!DNL Marketo Optimizer]. | _Adapte nuestro programa de nutrición para seminarios web empresariales del tercer trimestre de [!DNL Marketo Engage] a [!DNL Marketo Optimizer]._ |
| `ai-decisioning-health-marketo-optimizer` | Informe de si los datos del inquilino están listos para la toma de decisiones de IA, lo que abarca la cobertura de historias, la riqueza de rasgos y la cobertura personal. | _¿Qué datos se utilizan para la toma de decisiones de IA?_ |

### Ejemplo de solicitud de creación de programa {#program-creation-prompt}

Cargue una descripción breve o describa el programa directamente. Incluya la audiencia, el recorrido, el contenido y la configuración que desea que use [!DNL Coworker].

El diagrama resume las secciones de solicitud en el ejemplo siguiente. Muestra cómo organizar la solicitud, no el orden en que las personas se desplazan por el recorrido.

![Ocho secciones de solicitud de creación de programas: objetivo de programa, audiencia, recorrido con invitaciones basadas en la intención, contenido de correo electrónico, activación de LinkedIn, administración de registro, seguimiento posterior al evento y configuración.](./assets/coworker-program-creation-prompts.svg){width="800" zoomable="yes"}

Expanda cada sección para ver la solicitud de ejemplo.

+++Objetivo del programa

_Cree un programa de marketing B2B llamado Experience Cloud Leadership Forum: Experience Summit con tecnología de IA, que se celebrará del 3 de agosto al 3 de diciembre y utilizará el correo electrónico y LinkedIn. El evento es en el Centro de Innovación de la Bahía Área a las 9:00 AM. Iniciar el recorrido inmediatamente._

+++

+++Público

_Segmente a las personas con cualquier intención de producto para Experience Cloud y una puntuación de participación mayor que 1. Excluir perfiles cancelados y suspendidos por marketing._

+++

+++Recorrido

_Utilice la siguiente mejor ruta para dividir la audiencia por intención de Experience Cloud alta, Medium y baja. Envíe invitaciones personalizadas por correo electrónico adaptadas a cada nivel de intención. Combinar rutas y esperar dos días. Compruebe las aperturas de correo electrónico, los clics, la participación en el contenido y los registros. Envíe una vista previa de la agenda a los miembros comprometidos; active a los miembros no comprometidos en LinkedIn y espere dos días. Combine las rutas comprometidas y envíe un recordatorio de registro final 10 días antes del evento. Habilitar optimización del tiempo de envío para todos los correos electrónicos._

+++

+++Contenido de correo electrónico

_Crea tres correos electrónicos: Invitación ejecutiva (6 semanas antes del evento), Vista previa de la agenda (seis semanas antes del evento) y Recordatorio de registro final (10 días antes del evento). Incluya líneas de asunto, encabezados previos, llamadas a la acción (Reservar mi puesto, Ver agenda, Registro completo) y contenido personalizado con IA mediante historia de la persona, clasificación personal, sector, interés de la solución, participación reciente e intención de Experience Cloud. Incluya una imagen de lugar en la invitación, pero no un titular en la vista previa de la agenda._

+++

+++LinkedIn

_Segmente a los miembros no comprometidos con contenido patrocinado que promueva la transformación de la experiencia del cliente y la personalización de IA._

+++

+++Registro

_Salga inmediatamente del recorrido de invitación a los miembros registrados y envíe un correo electrónico de preparación para ejecutivos con temas de discusión generados por IA, una agenda personalizada, detalles del lugar de celebración, sesiones recomendadas y un vínculo al calendario._

+++

+++Posterior al evento

_Dirija a los asistentes al programa de seguimiento de liderazgo de Experience Cloud con un resumen, grabaciones, recursos y revisión de la calificación de ventas. Envíe eventos destacados de la cumbre, contenido bajo demanda e invitaciones a eventos futuros sin participación._

+++

+++Configuración

_Establezca my.replyToEmail en `events@example.com` y my.senderName en Eventos de Experience Cloud. Use una plantilla reutilizable en la que solo cambien la ciudad, el lugar de celebración, los temas principales y el enfoque del sector._

+++

Para obtener más información acerca de cómo preparar un informe, vea [Crear un programa a partir de un informe](./program-from-brief.md).

## Ejemplos de casos de uso {#use-cases}

### Cree un programa después de comprobar la preparación de los datos {#check-readiness-create-program}

Un posible cliente de operaciones de marketing desea saber que el inquilino está listo para la toma de decisiones de IA antes de crear un nuevo programa basado en cuentas.

1. Para revisar la cobertura de la historia, la riqueza de características y la cobertura personal, ejecuta la [comprobación de estado de decisiones de IA](./ai-decisioning-health.md). Por ejemplo, pregunte: _Mostrarme datos de Marketo aprovechados para la toma de decisiones de IA._
1. Aborde cualquier brecha que identifique el informe.
1. Cargue un informe de campaña y pregunte: _Cree un programa con el informe adjunto._
1. Revise y apruebe el programa cuando [!DNL Coworker] presente el resultado.

El resultado es un informe de preparación que identifica deficiencias, seguido de un programa basado en datos que pueden apoyar la toma de decisiones de IA.

### Mover un programa [!DNL Marketo Engage] existente a [!DNL Marketo Optimizer] {#adapt-program}

Un equipo de generación de demanda desea que un programa de eficacia demostrada se ejecute en [!DNL Marketo Optimizer] sin reconstruirlo manualmente.

1. Asigne un nombre al programa [!DNL Marketo Engage] que se va a adaptar. Por ejemplo: _Adapte el programa de nutrición del seminario web empresarial del tercer trimestre de [!DNL Marketo Engage] a [!DNL Marketo Optimizer]._
1. [!DNL Coworker] asigna el programa a [!DNL Marketo Optimizer] construcciones y marca todo lo que no se convierte.
1. Revise el resultado y apruébelo.

El resultado es un programa convertido para su revisión, además de una lista de artículos que requieren una decisión manual.

## [!DNL Marketo Optimizer] herramientas MCP {#mcp-tools}

Las aptitudes de [!DNL Coworker] llaman a las 37 herramientas siguientes en el servidor de Protocolo de contexto de modelo (MCP) de [!DNL Marketo Optimizer]. Cada nombre de herramienta lleva el prefijo `marketo-optimizer__`.

Esta referencia cubre las herramientas documentadas por las habilidades registradas, incluidas las habilidades de soporte utilizadas durante un flujo de trabajo. No indica el estado de implementación ni la frecuencia de uso. Los nombres de aptitudes de esta tabla siguen la referencia de la herramienta y pueden diferir de los nombres de aptitudes específicos del producto que se han indicado anteriormente.

| Herramienta | Habilidades | Finalidad |
| --- | --- | --- |
| `marketo-optimizer__get_workspace_root_tree` | `program-creation-marketo-optimizer` | Busque la zona de espacio de trabajo o la subcarpeta con nombre para un nuevo programa. |
| `marketo-optimizer__create_program` | `program-creation-marketo-optimizer` | Cree un programa en la zona o carpeta confirmada. |
| `marketo-optimizer__list_programs` | `program-creation-marketo-optimizer`, `landing-page-authoring` | Examine programas o encuentre dónde archivar una página de aterrizaje. |
| `marketo-optimizer__get_program` | `program-creation-marketo-optimizer` | Leer un programa por ID. |
| `marketo-optimizer__update_program` | `program-creation-marketo-optimizer` | Actualizar metadatos del programa, como su nombre. |
| `marketo-optimizer__create_program_token` | `program-creation-marketo-optimizer` | Cree o corrija un token de programa aprobado. |
| `marketo-optimizer__list_program_tokens` | `program-creation-marketo-optimizer` | Leer los tokens resueltos de un programa. |
| `marketo-optimizer__create_dynamic_people_list_with_rules` | `program-creation-marketo-optimizer` | Cree una lista de personas vinculada a un programa y genere reglas de audiencia a partir de una descripción. |
| `marketo-optimizer__list_people_journeys` | `adapt-program`; referencia compartida del complemento de canal | Compruebe si hay un conflicto en el nombre de un recorrido de destino, busque un recorrido existente después de un resultado no claro o examine los recorridos para ver si funcionan en el canal. |
| `marketo-optimizer__create_person_journey` | `program-creation-marketo-optimizer`, `adapt-program`, `channel-content-authoring` | Cree un recorrido vinculado a un programa, inicie un recorrido adaptado o cree un recorrido que falte para un canal de correo electrónico. |
| `marketo-optimizer__get_person_journey` | `program-creation-marketo-optimizer`, `adapt-program`; referencia compartida del complemento de canal | Lea un recorrido o su lienzo, compruebe las ediciones preestablecidas o busque un recorrido para el trabajo en el canal. |
| `marketo-optimizer__update_person_journey` | `adapt-program` | Anexe un paso de generación aprobado a la vez al recorrido de destino. |
| `marketo-optimizer__run_person_journey_simulation` | `program-creation-marketo-optimizer` | Validar un flujo de recorrido sin publicar. |
| `marketo-optimizer__run_program_qa` | `program-creation-marketo-optimizer` | Ejecute una comprobación de disponibilidad de solo lectura en el programa y sus recorridos. |
| `marketo-optimizer__create_channel` | `channel-content-authoring`; `program-creation-marketo-optimizer` y `image-to-html` mediante transferencia | Crear y vincular un canal. Para el correo electrónico, la primera llamada enumera las plantillas; la segunda utiliza la plantilla seleccionada para crear y vincular el correo electrónico. |
| `marketo-optimizer__get_channel` | `channel-content-authoring` | Lea un canal, incluyendo opcionalmente su asunto de correo electrónico y HTML. |
| `marketo-optimizer__list_channels` | `channel-content-authoring` | Examine los canales por tipo y, opcionalmente, filtrados por nombre. |
| `marketo-optimizer__update_channel_content` | `channel-content-authoring`; `image-to-html` mediante transferencia | Actualizar el asunto de un correo electrónico para HTML, incluida la aplicación de HTML convertido. |
| `marketo-optimizer__image_to_html` | `image-to-html` | Inicie una conversión de diseño de correo electrónico asincrónico y recupere el HTML editable. |
| `marketo-optimizer__list_asset_library_images` | `landing-page-authoring` | Busque imágenes de reemplazo para las ranuras de la página de aterrizaje. |
| `marketo-optimizer__add_asset_to_program_or_folder` | `landing-page-authoring` | Registre una nueva página de aterrizaje en el programa o la carpeta seleccionados de Optimizer. |
| `marketo-optimizer__get_person_story` | `personalization-engine-health` | Leer la historia de personalización de una persona por ID numérico. |
| `marketo-optimizer__get_persona_story` | `personalization-engine-health` | Lea la historia para ver el nombre exacto de una persona. |
| `marketo-optimizer__run_arbitration` | `personalization-engine-health` | Vuelva a puntuar y a seleccionar los recorridos para las personas que cumplen los requisitos después de una confirmación explícita. |
| `marketo-optimizer__get_arbitration_summary` | `personalization-engine-health` | Lea las estadísticas de resumen de la última ejecución de mediación. |
| `marketo-optimizer__get_arbitration_decisions` | `personalization-engine-health` | Leer las decisiones por persona de la última ejecución de mediación. |
| `marketo-optimizer__get_ai_decisioning_health_summary` | `ai-decisioning-health` | Busque el informe general de preparación del inquilino. |
| `marketo-optimizer__get_persona_distribution` | `ai-decisioning-health` | Informar sobre recuentos y porcentajes de personas. |
| `marketo-optimizer__get_people_without_personas` | `ai-decisioning-health` | Informar sobre la cantidad y la cuota de personas sin personalidad. |
| `marketo-optimizer__get_person_story_attribute_coverage` | `ai-decisioning-health` | Mida la cobertura de la categoría de rasgos e identifique los campos rellenados. |
| `marketo-optimizer__get_person_story_data_completeness` | `ai-decisioning-health` | Informe de la riqueza, integridad y variación de la historia por persona. |
| `marketo-optimizer__get_person_story_coverage` | `ai-decisioning-health` | Informar sobre la cobertura de la historia, las tendencias y la generación pendiente. |
| `marketo-optimizer__get_personalization_story_pipeline_status` | `ai-decisioning-health` | Leer el estado de la canalización, el historial de ejecución y la duración del informe. |
| `marketo-optimizer__get_person_story_refresh_backlog` | `ai-decisioning-health` | Contar historias esperando actualización porque los datos de origen cambiaron. |
| `marketo-optimizer__get_person_intent_signal_coverage` | `ai-decisioning-health` | Mida la intención del producto, la intención de la palabra clave y la cobertura de la actividad. |
| `marketo-optimizer__get_person_story_activity_coverage` | `ai-decisioning-health` | Informar sobre los campos de participación capturados y las tendencias de actividad agregadas. |
| `marketo-optimizer__get_person_audience_membership_distribution` | `ai-decisioning-health` | Indique el promedio y la distribución de las suscripciones a audiencias por persona. |
