---
title: Escuchar un nodo de evento
description: 'Configuración de la escucha de nodos de evento en Marketo Optimizer: establezca déclencheur de evento, aplique filtros opcionales y haga avanzar a las personas cuando se produzcan actividades o cambios en los datos.'
TQID: 'https://experienceleague.adobe.com/6v3i6M-Hhr2RAWrS68WaEVb8VJEzJZbD7vXOJOsjgc8'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
source-git-commit: bc370a501d3f8ff80ad846576b62504aca77f530
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 2%
---
# Escucha de un nodo de evento

Para llevar a la audiencia al siguiente paso del recorrido cuando se produzca un evento, agregue el nodo _Escuchar un evento_.

## Déclencheur de eventos {#event-triggers}

Defina los criterios de evento que activan el nodo de recorrido y mueven al miembro de la audiencia hacia adelante.

| Activadores | Descripción |
| -------- | ----------- |
| Brand Concierge | Actividades para posibles clientes que interactúan con [!DNL Brand Concierge]. |
| Correo electrónico | Actividades de correo electrónico para posibles clientes, incluidos envíos, envíos y participación. |
| Evento | Actividades interactivas de seminarios web para posibles clientes, como registro, asistencia e interacciones. |
| Oportunidades | Actividades relacionadas con registros de oportunidades asociados a posibles clientes o cuentas. |
| Aplicaciones de ventas | Actividades de posibles clientes relacionadas con [!DNL Sales Qualifier] o [!DNL Marketo Sales Insights]. |
| Otro | Actividades que no se incluyen en las categorías predefinidas, lo que proporciona flexibilidad para déclencheur de eventos personalizados o varios. |

>[!BEGINSHADEBOX]

**Actividades de Marketo Engage compatibles con déclencheur**

Al activarse en eventos, [!DNL Marketo Optimizer] admite actividades de la instancia [!DNL Marketo Engage] que está conectada como origen de datos.

>[!NOTE]
>
>Solo puede haber una instancia de [!DNL Marketo Engage] como origen de datos y está preconfigurada en el momento del aprovisionamiento de la instancia de [!DNL Marketo Optimizer].

Puede generar déclencheur de eventos en torno a las [!DNL Marketo Engage] actividades siguientes:

* **[!UICONTROL Rellena el formulario Marketo Engage]**: se activa cuando un posible cliente envía un formulario [!DNL Marketo Engage] especificado.
* **[!UICONTROL Visita la página web de Marketo Engage]**: se activa cuando un posible cliente con una cookie de seguimiento de Munchkin visita una página web especificada.
* **[!UICONTROL Clics en vínculo en página web de Marketo Engage]**: se activa cuando un posible cliente hace clic en un hipervínculo rastreado en una página web que tiene instalado el código de seguimiento de Munchkin [!DNL Marketo Engage].
* **[!UICONTROL Se ha entregado el correo electrónico de Marketo Engage]**. Se activa cuando el servidor de correo de un posible cliente (MX) devuelve una respuesta correcta (un mensaje 250 OK) al servidor emisor [!DNL Marketo Engage].
* **[!UICONTROL Rebotes de correo electrónico de Marketo Engage]**: se activa cuando un servidor de correo de destino rechaza un mensaje de correo electrónico de [!DNL Marketo Engage] enviado como un error permanente, como un usuario no válido o un dominio desconocido.
* **[!UICONTROL Marketo Engage email bounces soft]**: se activa cuando un servidor de correo de destino rechaza un mensaje de correo electrónico enviado de [!DNL Marketo Engage] como un problema temporal (como un servidor ocupado o un buzón lleno). [!DNL Marketo Engage] reintenta automáticamente los rebotes suaves hasta tres veces a través de los servidores MX antes de marcar los problemas.
* **[!UICONTROL Cancela la suscripción al correo electrónico de Marketo Engage]**: se activa cuando un posible cliente decide excluirse de los correos electrónicos de marketing no operativos. Cuando se activa, [!DNL Marketo Engage] actualiza automáticamente el valor de campo `Unsubscribed` del posible cliente a `true`, lo que los suprime de futuros envíos de correo electrónico estándar.
* **[!UICONTROL Abre el correo electrónico de Marketo Engage]**. Se activa cuando un posible cliente abre un correo electrónico [!DNL Marketo Engage] rastreado.
* **[!UICONTROL Clics en vínculo en el correo electrónico de Marketo Engage]**: se activa cuando un posible cliente hace clic en cualquier vínculo (o en un vínculo restringido específico) dentro de un correo electrónico de [!DNL Marketo Engage].

>[!ENDSHADEBOX]

## Filtros de eventos {#event-filters}

Puede incluir filtros para limitar los déclencheur de evento coincidentes en función de varios criterios:

| Filtros | Descripción |
| ------- | ----------- |
| Historial de actividad | Actividades basadas en condiciones que se evalúan utilizando uno o más elementos seleccionados |
| Brand Concierge | Actividades para posibles clientes que interactúan con [!DNL Brand Concierge]. |
| Atributos de la compañía | Atributos del perfil de empresa/cuenta, incluidos: <li>[!UICONTROL Ingresos anuales] <li>[!UICONTROL Nombre de la compañía] <li>[!UICONTROL País de facturación] <li>[!UICONTROL Sector] <li>[!UICONTROL Número de empleados] <li>[!UICONTROL Código SIC] <li>[!UICONTROL Estado] |
| Datos de intención | Atributos basados en datos de intención asociados al perfil de la persona. |
| Oportunidades | Estado y atributos basados en las oportunidades asociadas con el perfil de la persona, incluidos: <li>[!UICONTROL Tiene oportunidad] <li>[!UICONTROL Número de oportunidades] <li>[!UICONTROL Importe total de la oportunidad] <li>[!UICONTROL Se agregó a la oportunidad] <li>[!UICONTROL Se eliminó de la oportunidad] |
| Atributos de la persona | Atributos del perfil de persona B2B, incluidos: <li>[!UICONTROL Ciudad] <li>[!UICONTROL País] <li>[!UICONTROL Fecha de nacimiento] <li>[!UICONTROL Dirección de correo electrónico] <li>[!UICONTROL Correo electrónico no válido] <li>[!UICONTROL Correo electrónico suspendido] <li>[!UICONTROL Nombre] <li>[!UICONTROL Región de estado deducido] <li>[!UICONTROL Título de trabajo] <li>[!UICONTROL Apellido] <li>[!UICONTROL Número de teléfono móvil] <li>[!UICONTROL Puntuación de participación de personas] <li>[!UICONTROL Número de teléfono] <li>[!UICONTROL Código postal] <li>[!UICONTROL Estado] <li>[!UICONTROL Canceló la suscripción] <li>[!UICONTROL Motivo de cancelación de suscripción] |
| Aplicaciones de ventas | Actividades de posibles clientes relacionadas con [!DNL Sales Qualifier] o [!DNL Marketo Sales Insights]. |
| Filtros especiales | Filtrado de atributos que no se incluyen en las categorías predefinidas, lo que proporciona flexibilidad para criterios de filtro personalizados o diversos. |

>[!BEGINSHADEBOX]

**Actividades de Marketo Engage compatibles con los filtros**

Al filtrar por eventos activados, [!DNL Marketo Optimizer] admite actividades de la instancia [!DNL Marketo Engage] conectada como origen de datos.

>[!NOTE]
>
>Solo puede haber una instancia de [!DNL Marketo Engage] como origen de datos y está preconfigurada en el momento del aprovisionamiento de la instancia de [!DNL Marketo Optimizer].

Puede generar filtros de eventos en torno a las [!DNL Marketo Engage] actividades siguientes:

* **[!UICONTROL Se ha completado el formulario de Marketo Engage]**. Coincide con los posibles clientes que han completado un formulario [!DNL Marketo Engage] específico en cualquier momento de su registro de actividades que no hayan caducado.
* **[!UICONTROL Visitó la página web de Marketo Engage]**. Coincide con los posibles clientes que vieron una dirección URL específica en su sitio web o en [!DNL Marketo Engage] páginas de aterrizaje. Se basa directamente en el código de seguimiento de Munchkin instalado en el sitio.
* **[!UICONTROL Se hizo clic en un vínculo en la página web de Marketo Engage]**. Coincide con los posibles clientes que han hecho clic en un vínculo o recurso específico de una página rastreada.
* **[!UICONTROL Se envió el correo electrónico de Marketo Engage]**. Coincide con los posibles clientes a los que [!DNL Marketo Engage] intentó enviar un correo electrónico específico, teniendo en cuenta las acciones de implementación anteriores a las devoluciones graves o las aceptaciones del servidor.
* **[!UICONTROL Se entregó el correo electrónico de Marketo Engage]**. Coincide con los posibles clientes cuyo servidor de correo (MX) devolvió una respuesta correcta (un mensaje 250 OK) al servidor emisor [!DNL Marketo Engage].
* **[!UICONTROL Correo electrónico de Marketo Engage devuelto]**: coincide con los posibles clientes que experimentaron un rechazo grave (error de envío permanente) en un envío de correo electrónico específico o dentro de un intervalo de tiempo.
* **[!UICONTROL El correo electrónico de Marketo Engage rebotó de forma suave]**. Coincide con los posibles clientes cuyos correos electrónicos experimentaron un error de entrega temporal (como una bandeja de entrada completa o un servidor sin conexión) en lugar de un rebote duro permanente.
* **[!UICONTROL Se canceló la suscripción al correo electrónico de Marketo Engage]**. Coincide con los posibles clientes que se excluyeron de los correos electrónicos de marketing no operativos. Cuando esto sucede, [!DNL Marketo Engage] actualiza automáticamente el valor de campo `Unsubscribed` del posible cliente a `true`, lo que los suprime de futuros envíos de correo electrónico estándar.
* **[!UICONTROL Correo electrónico de Marketo Engage abierto]** - Coincide con los posibles clientes que abrieron un correo electrónico de [!DNL Marketo Engage] rastreado.
* **[!UICONTROL Se hizo clic en un vínculo en el correo electrónico de Marketo Engage]**. Coincide con los posibles clientes que hicieron clic en un vínculo (o en un vínculo específico) incluido en un correo electrónico de [!DNL Marketo Engage].

>[!ENDSHADEBOX]

## Adición de un nodo de evento {#add-event-node}

1. Navegue hasta el lienzo de recorrido.

1. Haga clic en el icono de signo más (**+** ) en una ruta y elija **[!UICONTROL Escuchar un evento]**.

   ![Haga clic en agregar icono en la ruta de recorrido](./assets/person-journey-canvas-add-node.png){width="200"}

1. En las propiedades del nodo, a la derecha, haga clic en **[!UICONTROL Agregar criterios de evento]**.

1. En el cuadro de diálogo _[!UICONTROL Editar evento]_, agregue un evento y establezca las restricciones que desee que coincidan con el déclencheur.

   Arrastre y suelte el déclencheur de evento en el espacio del generador y establezca la definición. Haga clic en **[!UICONTROL Agregar restricción]** para cada restricción que desee usar para restringir la coincidencia de eventos.

   ![Editar evento: déclencheur de evento](./assets/edit-event-triggers.png){width="700" zoomable="yes"}

   Puede añadir varios eventos para que coincidan. El primer evento de calificación hace avanzar el perfil de la persona en el recorrido.

1. (Opcional) Seleccione la ficha **[!UICONTROL Filtros]** y agregue criterios de filtrado para los déclencheur.

   Arrastre y suelte el filtro en el espacio del generador y establezca la definición. Haga clic en **[!UICONTROL Agregar restricción]** para cada restricción que desee usar para restringir la coincidencia de filtros.

   ![Editar evento: filtrado de eventos](./assets/edit-event-filters.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Guardar]**.

   En cualquier momento, puede hacer clic en **[!UICONTROL Editar evento]** para cambiar los criterios del evento para el nodo.

1. Si es necesario, establezca la opción **[!UICONTROL Tiempo de espera]** para limitar el período de tiempo durante el cual se escuchará el evento.

   >[!NOTE]
   >
   >El recorrido finaliza después de un tiempo de espera a menos que defina una ruta de tiempo de espera, donde puede agregar otros nodos.

   Habilite la opción **[!UICONTROL Tiempo de espera]** y seleccione el período de tiempo durante el cual el recorrido espera a que se produzca un evento antes de que se agote el tiempo de espera.

   ![Opciones de tiempo de espera habilitadas para el nodo Escuchar recorrido de eventos](./assets/person-journey-event-node-timeout.png){width="550" zoomable="yes"}

   Puede elegir finalizar la ruta aquí o realizar una acción diferente estableciendo otra ruta. Para crear una nueva ruta en el recorrido donde se puedan agregar acciones y eventos aplicables a los perfiles cuando no se produzca el evento, active la casilla de verificación **[!UICONTROL Establecer ruta de tiempo de espera]**.
