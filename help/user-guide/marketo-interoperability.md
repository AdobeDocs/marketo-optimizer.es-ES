---
title: Interoperabilidad con Marketo Engage
description: Descubra lo que Marketo Optimizer comparte con Marketo Engage, incluidos datos, actividades y audiencias, y cómo enviar correos electrónicos desde cualquier producto en sus recorridos.
role: User, Admin
autotag-review: '2026-10-01T18:40:01.444Z'
TQID: 'https://experienceleague.adobe.com/7TB6JG9yiUT-l0VevNW4tvwieCyFjOypZwI0SlUzmmY'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
  - id: 46e599c6-e20f-5f67-9824-93415016f66b
    internal-label: Audiences
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
    internal-label: Journeys
  - id: a29661b8-f7a4-53d1-a9ac-fdec08c092e4
    internal-label: Programs
  - id: d4203578-d294-5145-b397-f26f4488a904
    internal-label: Channels
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: 518a807aeed2471772b4f0a4d6d8d525cd3e22fd
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%
---

# Interoperabilidad con Marketo Engage

[!DNL Adobe Marketo Optimizer] y [!DNL Adobe Marketo Engage] comparten datos, algunas actividades y audiencias. Mantienen los recursos separados. Comprenda qué comparte cada producto para decidir dónde generar y enviar su marketing.

## Compartido entre los productos {#shared}

* [!DNL Marketo Engage] posibles clientes y actividades fluyen automáticamente a [!DNL Marketo Optimizer].
* Los recorridos pueden escuchar [!DNL Marketo Engage] actividades.
* Las audiencias basadas en eventos pueden incluir a personas que realizan [!DNL Marketo Engage] actividades.
* Las acciones de recorrido pueden interactuar con [!DNL Marketo Engage]. Puede agregar o quitar personas de una lista [!DNL Marketo Engage] y solicitar una campaña [!DNL Marketo Engage].
* [!UICONTROL Scoring Studio] puntúa a las personas en [!DNL Marketo Engage] y [!DNL Marketo Optimizer] actividades. Puede usar las puntuaciones de [!DNL Marketo Engage].
* Ambos productos comparten direcciones IP y subdominios.
* Los informes conversacionales unificados abarcan ambos productos.

## Se mantienen separados {#separate}

* **Assets:** correos electrónicos, plantillas, programas e imágenes se encuentran en repositorios separados.
* **Actividades:** Las actividades de [!DNL Marketo Optimizer] no se han compartido de nuevo en [!DNL Marketo Engage].
* **Campos y límites:** Los campos personales que [!DNL Marketo Optimizer] deriva no están disponibles en [!DNL Marketo Engage]. Los límites de comunicación se establecen por separado en cada producto.

Para obtener detalles de sincronización, vea [Sincronización de entidades](./data-architecture.md#entity-sync).

## Enviar correo electrónico desde Marketo Engage {#send-from-marketo}

Utilice este método para ejecutar recorridos, pasos de espera y toma de decisiones de IA en [!DNL Marketo Optimizer] mientras [!DNL Marketo Engage] envía cada correo electrónico.

1. En [!DNL Marketo Optimizer], cree un recorrido que incluya pasos de espera y toma de decisiones de IA.
1. Para cada paso de envío, agregue la acción **[!UICONTROL Solicitar campaña de Marketo Engage]** y seleccione una campaña [!DNL Marketo Engage] que corresponda.
1. Opcional: agregue un programa predeterminado y global en [!DNL Marketo Engage] para agregar los informes de éxito en el recorrido.

Para obtener información sobre la acción, consulte [Realizar una acción en el nodo](./marketing/action-nodes.md).

[!DNL Marketo Engage] envía el correo electrónico a través de la configuración de canal existente. Debido a que [!DNL Marketo Engage] envía el correo electrónico, usted no configura canales ni correos electrónicos en [!DNL Marketo Optimizer]. Además:

* Los envíos, aperturas y clics se registran en [!DNL Marketo Engage].
* Se aplica la administración de cancelación de suscripción y el control de correo electrónico en [!DNL Marketo Engage].
* La actividad de correo electrónico alimenta las campañas de puntuación [!DNL Marketo Engage] existentes.
* Las campañas de sincronización de Salesforce activadas por la actividad se ejecutan según lo esperado.
* Cada envío se asigna a una campaña [!DNL Marketo Engage], por lo que puede realizar un seguimiento de los miembros del programa por campaña de correo electrónico e informar en programas conocidos.

## Enviar correo electrónico desde Marketo Optimizer {#send-from-optimizer}

Utilice este método para generar el recorrido y enviar correo electrónico en su totalidad en [!DNL Marketo Optimizer]. [!DNL Marketo Engage] sigue siendo el sistema de registro para la transferencia a su sistema de administración de la relación con los clientes (CRM).

1. Configure el canal de correo electrónico. Cree plantillas de correo electrónico, y configure la dirección IP y el subdominio, los vínculos de cancelación de suscripción y las páginas de aterrizaje. Ver [Capacidad de entrega de correo electrónico](./start/email-deliverability.md).
1. Establecer límites de comunicación en [!DNL Marketo Optimizer]. Los límites de comunicación compartida no están disponibles.
1. Cree el recorrido con audiencias, decisiones de IA y la siguiente mejor ruta.
1. Enviar correo electrónico desde [!DNL Marketo Optimizer]. [!DNL Marketo Optimizer] registra las actividades.
1. Puntúe a las personas en [!UICONTROL Scoring Studio] para crear un modelo en la actividad [!DNL Marketo Engage] y [!DNL Marketo Optimizer]. Consulte [Estudio de puntuación](./labs/scoring-studio.md).

Cancela la suscripción de sincronizar automáticamente con [!DNL Marketo Engage] mediante campos compartidos. [!DNL Marketo Optimizer] la actividad de correo electrónico no se ha devuelto a [!DNL Marketo Engage], pero [!UICONTROL Scoring Studio] todavía la usa.

### La entrega lleva a las ventas {#hand-off}

[!DNL Marketo Optimizer] no tiene integración directa con CRM. La ruta lleva a través de [!DNL Marketo Engage] con uno de estos métodos:

* **Basado en puntuación:** El campo de puntuación aparece en [!DNL Marketo Engage], y una campaña inteligente sincroniza el posible cliente con su CRM.
* **Basado en actividades:** Un recorrido de [!DNL Marketo Optimizer] escucha la actividad y agrega el posible cliente a una campaña inteligente de [!DNL Marketo Engage].
* **Suscripción al programa:** El recorrido se encuentra en un programa [!DNL Marketo Optimizer], por lo que realiza el seguimiento del estado de principio a fin.
