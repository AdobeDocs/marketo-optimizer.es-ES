---
title: Promoción de seminarios web y Recorridos de seguimiento
description: Cree recorridos promocionales, de día de envío y posteriores al seminario web en torno a un seminario web en Marketo Optimizer y personalice el contenido con tokens de seminario web.
keywords: 
role: User
feature: Person Journeys
TQID: 'https://experienceleague.adobe.com/9NJrT-Y66XXF1-mWDO80WpymCB6ujrkjkR87MhKuiB8'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 823
ht-degree: 0%

---


# Promoción de seminarios web y recorridos de seguimiento

Después de agregar un seminario web a un programa, compila uno o más [recorridos](./person-journeys.md) dentro del mismo programa para invitar a otras personas, recordarles, entregar la sesión y hacer un seguimiento después.

>[!NOTE]
>
>Esta página cubre la construcción de estos recorridos a mano. Para que el Compañero cree los mismos recorridos a partir de una plantilla, consulte [Crear seminarios web con el Compañero](../agents/webinar-creation.md).

## Creación de un recorrido de promoción {#build-promotion-journey}

Un recorrido de promoción típico invita a las personas, rastrea su registro y les recuerda a medida que se acerca el seminario web.

1. [Crear el recorrido de persona](./person-journeys.md#create-a-person-journey).

1. [Seleccione una audiencia para el recorrido](./person-audience-node.md).

1. Agregue un nodo **[!UICONTROL Enviar correo electrónico]** con un correo electrónico de invitación.

   Use tokens de seminarios web como _Title_ y _Start Datetime_ en el contenido y vincule a la página de registro del seminario web.

1. Agregue un nodo **[!UICONTROL Realizar una acción]**, seleccione la acción **[!UICONTROL Cambiar estado de miembro del seminario web]**, seleccione el seminario web y establezca el estado en _Invitado_.

   Colóquelo inmediatamente después del nodo **[!UICONTROL Enviar correo electrónico]** de la invitación.

   >[!NOTE]
   >
   >Por lo general, solo se establece _Invitado_ y _Registrado_ a partir de un recorrido de promoción. [!DNL Adobe Connect] normalmente establece _Asistió_, _No se presentó_ y _Asistió a petición_ automáticamente. La misma acción puede anular estos estados posteriores de un recorrido si es necesario, pero solo hacia adelante, si coincide con la progresión lineal descrita en [_Estado del seminario web_](webinars-overview.md#webinar-status).

1. Aloje el formulario de registro en una [página de aterrizaje](../content/landing-pages.md).

1. Agregue un nodo **[!UICONTROL Realizar una acción]**, seleccione la acción **[!UICONTROL Cambiar el estado de miembro del seminario web]**, seleccione el seminario web y establezca el estado en _Registrado_ (activado por el envío del formulario).

   Mover a alguien a _Registrado_ hace dos cosas automáticamente:

   * [!DNL Adobe Connect] genera la URL de unión individual de esa persona.
   * Envía el correo electrónico de confirmación, si lo ha configurado, que contiene el token _Uniéndose a la URL_.

1. Cree una cadencia de recordatorio usando **[!UICONTROL Esperar]** nodos cronometrados en relación con el token del seminario web _Iniciar fecha y hora_.

   Por ejemplo, establézcalo en una semana antes, un día antes y una hora antes.

1. Se ha superado el tiempo de espera de un nodo **[!UICONTROL Wait]** al token _End Datetime_ del seminario web, por lo que el recorrido se pausa hasta que finaliza la sesión activa.

   Continúe con [Crear un recorrido posterior al seminario web](#build-post-webinar-journey) desde aquí.

   >[!NOTE]
   >
   >Los cambios de estado del seminario web no están disponibles actualmente como déclencheur de **[!UICONTROL Escuchar un evento]**. En su lugar, use un nodo **[!UICONTROL Wait]** con tiempo de espera seguido de un nodo **[!UICONTROL Split paths]** en el estado del seminario web, como se muestra a continuación, en lugar de escuchar el cambio de estado en sí.

## Personalizar correos electrónicos

Los tokens de seminario web se representan en el contenido del correo electrónico: asunto, cuerpo, encabezado previo y remitente. Consulte [tokens de seminario web](webinars-overview.md#webinar-tokens) para obtener la lista completa.

>[!NOTE]
>
>Actualmente, los tokens de seminario web no están disponibles en la página de aterrizaje de registro ni en los formularios. Personalice los que tengan tokens de programa estándar en su lugar y reserve una personalización específica del seminario web (como la URL de unión y la URL de grabación) para correo electrónico.

>[!IMPORTANT]
>
>El token **_Unirse a la URL_** solo se resuelve para las personas cuyo estado de seminario web sea _Registrado_ o posterior. El token de **_URL de grabación_** solo se resuelve después de que se publique la grabación. Ambos se resuelven en un valor vacío de antemano en lugar de en un error, por lo que vuelva a comprobar que los correos electrónicos se representan de forma aceptable antes de publicar.

## Impartir el seminario web {#deliver-webinar}

A la hora programada, el seminario web se ejecuta en [!DNL Adobe Connect]:

* Los presentadores y co-presentadores se unen usando su enlace individual en la sección **Equipo de seminarios web** del seminario web.
* Los asistentes se unen usando su token personal **Uniéndose a la URL**.
* [!DNL Adobe Connect] captura la actividad durante la sesión (preguntas, respuestas de sondeo, clics en vínculos, descargas de recursos y subidas manuales) y la envía de vuelta a [!DNL Marketo Optimizer] como [actividades de seminarios web](webinars-overview.md#webinar-activities), disponibles para cualquier recorrido de escucha.

Si el seminario web está establecido en **Simulación en vivo**, el contenido pregrabado se reproduce automáticamente a la hora programada mientras los presentadores participan en vivo a través del chat, las encuestas y las preguntas y respuestas.

## Creación de un recorrido posterior al seminario web {#build-post-webinar-journey}

Una vez finalizada la sesión activa, [!DNL Adobe Connect] establece el estado del seminario web de cada persona en _Asistido_ o _No mostrado_. Cuando se libere el nodo de recorrido **[!UICONTROL Wait]**, la rama que usa ese estado con un nodo **[!UICONTROL Split paths]**.

1. Agregue un nodo de **[!UICONTROL rutas divididas]** con una condición en el estado del seminario web, como _Ha asistido al seminario web_.

1. En la ruta _Asistió_, envíe un correo electrónico de agradecimiento.

   Por ejemplo, envíe una reproducción y un seguimiento de recursos. A continuación, utilice un nodo **[!UICONTROL Wait]** y un correo electrónico de call-to-action del paso siguiente.

1. En la ruta _No mostrar_, envía un correo electrónico _te hemos perdido_.

   En el contenido del correo electrónico, invítelos a ver la grabación. A continuación, utilice un nodo **[!UICONTROL Wait]** y un correo electrónico de seguimiento que resuma los aspectos clave.

1. Personalice cualquiera de las dos rutas más mediante otras actividades de seminario web.

   Por ejemplo, bifurcar o personalizar según _Responde a una encuesta_ con una respuesta específica.

1. Use el token de la dirección URL **_grabación_** en cualquiera de las rutas una vez que se pueda resolver, para que los demás puedan verlo bajo demanda.

   **_La participación bajo demanda_** (duración del reloj, clics en vínculos de reproducción y descargas) se ingiere como las mismas actividades del seminario web, etiquetadas con un modo de _Bajo demanda_. A diferencia de esas actividades, la visualización bajo demanda también mueve a una persona _No se presenta_ al estado del seminario web _Asistió bajo demanda_. Como resultado, una ruta de recorrido de _No mostrar_ puede llegar a las personas que vean la grabación más tarde. Continúe dividiendo el estado del seminario web o vuelva a comprobarlo después de un retraso si desea un tratamiento diferente para las personas que lo ven bajo demanda.
