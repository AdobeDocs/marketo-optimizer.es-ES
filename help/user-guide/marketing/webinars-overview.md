---
title: Seminarios web interactivos
description: Conozca los conceptos subyacentes a los seminarios web interactivos en Marketo Optimizer, incluido el modelo de recursos de seminarios web, los estados miembros, los tokens y las actividades.
keywords: 
role: User
feature: Channels
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: 1085
ht-degree: 2%

---


# Seminarios web interactivos

Los seminarios web interactivos le permiten planificar, promocionar, entregar y realizar el seguimiento de un seminario web en vivo o en vivo simulado sin salir de [!DNL Adobe Marketo Optimizer]. La entrega se ejecuta en [!DNL Adobe Connect] automáticamente, por lo que nunca tendrá que cambiar de producto para diseñar una página de registro, organizar la sesión en vivo o extraer los datos de asistencia.

>[!NOTE]
>
>Esta función requiere una licencia y está sujeta a términos y condiciones adicionales. Para obtener más información sobre los términos y condiciones adicionales, revise el contrato o póngase en contacto con Adobe.

Puede crear un seminario web de dos formas:

* **Experiencia de conversación** - Pida al compañero que programe, promueva e informe sobre un seminario web en lenguaje natural. Ver [Creación de seminarios web con el compañero](../agents/webinar-creation.md).

* **Apuntar y hacer clic**: use el área de trabajo de _[!UICONTROL Programas]_ para agregar un recurso de seminario web, diseñarlo, agregar presentadores y copatrocinadores, crear recorridos de promoción y seguimiento y revisar la creación de informes. Ver [Crear y diseñar un seminario web](create-webinar.md) y [recorridos de seguimiento y promoción de seminarios web](webinar-journeys.md).

## Seminario web como recurso

Un seminario web es un recurso que pertenece a un [programa](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/prime/marketing-management/programs/programs), del mismo modo que un correo electrónico o una página de aterrizaje. Al agregar un seminario web a un programa, se registra allí y sus tokens, atributos y actividades están disponibles para todos los recorridos y recursos de ese programa.

>[!IMPORTANT]
>
>Un programa puede tener actualmente un recurso de seminario web. En una versión futura se prevé la compatibilidad con varios seminarios web por programa.

## Estados miembros

Para cualquier persona que sea miembro de un programa que contenga un seminario web, se aplican tres estados independientes al mismo tiempo. Se puede hacer referencia a cada uno por separado en las audiencias y condiciones de recorrido.

| Estado | Propietario | Valores |
|---|---|---|
| Estado de miembro del programa | Programa | Configurable por [tipo de programa](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/prime/admin/program-types) |
| Estado del seminario web | Recurso de seminario web | Invitado, Registrado, Asistido, No presentarse, Asistido a petición |
| estado de recorrido | Recorrido | Estado del nodo actual, en pausa, completado y otros estados de tiempo de ejecución de recorrido |

### Estado del seminario web

El estado del seminario web tiene cinco valores. [!DNL Adobe Connect] normalmente establece el valor automáticamente, pero también puede establecer el estado con una acción de recorrido si necesita anularlo. Para reflejar la asistencia registrada en otro sistema, por ejemplo, puede establecer el estado en el recorrido.

| Estado | Cómo se establece | Origen |
|---|---|---|
| Invitado | Un nodo de recorrido _Realizar una acción_, normalmente cuando se envía el correo electrónico de invitación | Controlado por el autor |
| Registrado | Un nodo de recorrido _Realizar una acción_ cuando la persona se registre. Esto también envía a [!DNL Adobe Connect] al déclencheur para generar la dirección URL de unión de la persona | Controlado por el autor |
| Asistió | Un evento de [!DNL Adobe Connect] después de que se ejecute el seminario web en directo | Controlada por el sistema, con anulación de autor disponible mediante un recorrido |
| No-Show | Un evento de [!DNL Adobe Connect] después de que se ejecute el seminario web en directo | Controlada por el sistema, con anulación de autor disponible mediante un recorrido |
| Asistencia bajo demanda | Evento de [!DNL Adobe Connect] en el que una persona que no asistió se muestra la grabación | Controlada por el sistema, con anulación de autor disponible mediante un recorrido |

>[!IMPORTANT]
>
>Ya sea que se establezca automáticamente o desde un recorrido, el estado del seminario web solo se mueve en una dirección, del mismo modo que [estado del programa](./programs.md#statuses). Una persona puede pasar a un estado posterior (por ejemplo, _Registrada_ a _Asistida_), pero no a uno anterior. Planifique cualquier anulación de autor teniendo en cuenta esta progresión lineal.

Para mover a una persona de un recorrido a otro estado, usa la acción **[!UICONTROL Cambiar estado de miembro del seminario web]**. Ver [recorridos de seguimiento y promoción de seminarios web](webinar-journeys.md).

## Tokens de seminario web

Los tokens de seminario web están disponibles en cualquier lugar donde personalice el contenido del correo electrónico (asunto, cuerpo, encabezado previo y remitente). Encuéntralos en el editor de personalización en **_Contexto > Seminario web_**.

Los tokens de nivel de recurso se sientan directamente en la carpeta del seminario web:

&#x200B;- Título
&#x200B;- Descripción
&#x200B;- Fecha y hora de inicio y fecha y hora de finalización
&#x200B;- Duración
&#x200B;- Zona horaria
&#x200B;- Presentadores
&#x200B;- URL de grabación

>[!NOTE]
>
>Los hosts compartidos se muestran en la sección Equipo del seminario web de la página del seminario web, pero no están disponibles como token de personalización.

Los tokens de cada destinatario se encuentran en una subcarpeta **Member**:

&#x200B;- **Estado** - El estado actual del seminario web del destinatario (Invitado, Registrado, Asistido, Sin presencia o Asistido bajo demanda). Ver [estado del seminario web](#webinar-status).
&#x200B;- **Unirse a la dirección URL**: vínculo personal [!DNL Adobe Connect] del destinatario. Esto solo se resuelve después de que el estado del seminario web del destinatario sea Registrado o posterior. Se resuelve en blanco para cualquiera en una etapa anterior.
&#x200B;- **URL de grabación**: se resuelve después de que se publique la grabación después de la sesión en directo y permanece vacía hasta entonces. Utilícelo de forma condicional en los correos electrónicos posteriores al seminario web para que no aparezca un vínculo antes de que se muestre una grabación.

>[!NOTE]
>
>Actualmente, los tokens de seminario web solo se representan en el contenido del correo electrónico (asunto, cuerpo, encabezado previo y remitente). La compatibilidad con los tokens de seminarios web en páginas de aterrizaje y formularios está planificada para una versión futura.
>
>Dado que estos tokens se resuelven como vacíos en lugar de generar un error, un correo electrónico o una página que haga referencia a ellos se procesará de forma segura en cualquier momento del ciclo de vida del seminario web. Previsualice el contenido antes y después de que los valores estén disponibles para confirmar que el diseño tiene el aspecto adecuado en cualquier caso.

## Actividades de seminario web

Cada seminario web informa automáticamente de las actividades que puede usar como déclencheur de _Escuchar eventos_, condiciones de _Ruta dividida_, filtros de audiencia y métricas de informes:

* Hace una pregunta
* Responde a una encuesta
* Hace clic en un vínculo
* Descarga un recurso
* Levanta una mano

>[!NOTE]
>
>Los cambios de estado del seminario web (Invitado, Registrado, Asistido, No presentarse, Asistido bajo demanda) no están disponibles actualmente como su propio déclencheur de actividad o _Escuchar evento_. Para bifurcar un recorrido en el estado del seminario web, usa una condición _Split path_ en el estado del seminario web directamente (tal y como se describe en [_Crear un recorrido posterior al seminario web_](webinar-journeys.md#build-post-webinar-journey)) en lugar de escuchar una actividad de cambio de estado.

La participación de las personas que ven la grabación después del evento en directo se ingiere como las mismas actividades, etiquetadas con un modo de On-Demand. A diferencia de las actividades, la participación a petición crea un estado de seminario web independiente: una persona que no asistió en directo y luego ve el movimiento de grabación de **No se presentó** a **Asistió a petición**.

## Requisitos previos

Antes de empezar a crear un seminario web, asegúrese de que lo siguiente esté listo.

| Requisito previo | Detalles |
|---|---|
| Un programa | El seminario web se agrega dentro de un programa existente. Un analista de operaciones de marketing suele crear primero el programa. |
| Licencia para seminario web (capacidad) | Debe haber disponible una licencia de seminario web, también denominada asignación de capacidad, antes de poder programar un seminario web. Usted elige una capacidad en el momento de la configuración, y los complementos de mayor capacidad pueden estar disponibles. Para aumentar la capacidad disponible, póngase en contacto con el equipo de su cuenta de Adobe. |
| [!DNL Adobe Connect] | El envío se ejecuta en [!DNL Adobe Connect]. El aprovisionamiento se produce automáticamente en segundo plano. No necesita dejar [!DNL Marketo Optimizer] para crear o alojar un seminario web. |

### Permisos

El acceso a las funciones de los seminarios web depende de los permisos asignados para ellos.

| Función | Qué concede |
|---|---|
| Ver seminarios web B2B | Vea la lista de seminarios web y una configuración, detalles e informes de seminarios web. Los controles Crear, Diseñar, Editar e Introducir no están disponibles mediante este permiso y no se le puede asignar a un seminario web como copatrocinador o presentador. |

<!-- 
| Manage B2B webinars | Full lifecycle access: create, design, configure, schedule, edit, deliver, host, and delete a webinar. The Create, Design, Edit, and Manage controls are available only for users with this role. |
| Webinar co-host | After you are added as a co-host, this permission enables you to design and enter that webinar with co-host controls. |
| Webinar presenter | After you are added as a presenter, this permission enables you to view and enter that webinar with presenter capabilities. It grants no authoring or design access on its own. |

>[!NOTE]
>
>Co-hosts and presenters are currently defined by entering a name and email rather than selected from a picker of role-eligible users — see [Add co-hosts and presenters](create-webinar.md#add-co-hosts-and-presenters). The _Webinar co-host_ and _Webinar presenter_**_ roles still govern what that person can do when they are added as a co-host or presenter.

-->
