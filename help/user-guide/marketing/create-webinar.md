---
title: Creación y diseño de un seminario web
description: Agregar un recurso de seminario web a un programa, diseñarlo en  [!DNL Adobe Connect], agregar co-hosts y presentadores, ejecutar una sesión de prueba y editar un seminario web en directo en  [!DNL Marketo Optimizer].
keywords: 
role: User
feature: Channels
TQID: 'https://experienceleague.adobe.com/fFvlOnp8hDF1RNOyohPWkc1whSG3T3deNrJ3RnEDzlo'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: a29661b8-f7a4-53d1-a9ac-fdec08c092e4id: d4203578-d294-5145-b397-f26f4488a904
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 680
ht-degree: 0%

---


# Creación y diseño de un seminario web

Agregue un seminario web a un programa, diseñe su registro y experiencia en la sala, y asígnele personal con los copatrocinadores y presentadores dentro de [!DNL Marketo Optimizer]. Antes de comenzar, revise [información general sobre seminarios web interactivos](webinars-overview.md) para conocer los conceptos subyacentes a los estados, tokens y funciones de los seminarios web, y confirme que tiene la función **Crear y administrar seminarios web**.

## Añadir un seminario web a un programa

1. Busque primero el programa en la estructura de árbol _[!UICONTROL Programas]_ o [cree un programa](./programs.md#create-program).

1. Haga clic en el icono _Menú más_ ( **...** ) junto al nombre del programa y seleccione **[!UICONTROL Crear seminario web]**.

1. En el cuadro de diálogo, introduzca los detalles principales del seminario web:

   * **Título** y **Descripción**.
   * **Horario**: fecha y hora de inicio, zona horaria y duración.
   * **Audiencia máxima**: la capacidad de licencia del seminario web que se utilizará en esta sesión.

   ![Cuadro de diálogo Programar seminario web con campos para el programa principal, nombre, duración, zona horaria, hora de inicio y audiencia máxima, además de los botones Cancelar y Crear.](assets/webinar-create-schedule-dialog.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >La entrega de una sola sesión frente a la recurrente y las opciones de audio/vídeo no se pueden configurar actualmente. Cada seminario web es una sola sesión habilitada para vídeo.

1. Agregar **co-hosts** y **moderadores**.

   >[!NOTE]
   >
   >En la versión actual, agregará a todos como contactos externos por nombre y correo electrónico, tengan o no una cuenta SSO de Adobe apta para roles.<!-- See [Permissions](./webinars-overview.md#permissions) for what each role governs. --> Para ver los pasos completos, consulte [_Agregar presentadores y co-hosts_](#add-co-hosts-and-presenters).

1. (Opcional) Personalice la plantilla, la marca y el diseño de la sala.

   Estas opciones se administran en [!DNL Adobe Connect] y también se pueden refinar más adelante desde la superficie de diseño. Ver [Diseño del seminario web](#design-the-webinar).

1. Haga clic en **[!UICONTROL Guardar]**.

   Guardar registra el seminario web en el programa y pone sus tokens, atributos y actividades a disposición de todos los recorridos y recursos de ese programa.

>[!NOTE]
>
>La creación de seminarios web equivale a _seminarios web interactivos_ en [!DNL Marketo Engage], por lo que los campos son familiares si ha realizado esto a través de esa aplicación.

## Diseño del seminario web {#design-the-webinar}

Para abrir la superficie de diseño [!DNL Adobe Connect], incrustada directamente en [!DNL Marketo Optimizer], donde configurará la sala, la página de registro y los diseños, use _[!UICONTROL Diseñar su seminario web]_.

1. En la página del seminario web, haga clic en **Diseñar el seminario web**.

1. Elija un **modo de envío**:

   - **En vivo**: los moderadores organizan la sesión en tiempo real.
   - **Simulación en vivo**: el contenido pregrabado se reproduce a la hora programada, junto con el chat en vivo, las encuestas y las preguntas y respuestas.

1. Elija una **sala de seminarios web**.

   Cree una nueva sala o reutilice una existente.

1. Seleccione una **plantilla**, **idioma** y **tema** y, a continuación, obtenga una vista previa del diseño.

1. Agregue y organice los pods según sea necesario.

   Los pods disponibles incluyen Compartir, Notas, Vídeo, Chat, Lista de asistentes, Archivos, Vínculos web, Encuestas, Preguntas y respuestas y Encuesta.

1. Entre en la sala para revisar la experiencia y, a continuación, salga cuando haya terminado.

1. Guarde los cambios.

   Se muestra una confirmación para indicar que el seminario web se ha diseñado correctamente.

>[!TIP]
>
>Diseñe el seminario web antes de agregar coanfitriones y presentadores, de modo que el acceso y los controles se apliquen a la sala finalizada.

La personalización de salas, como logotipos, colores y fondos virtuales, se controla directamente en [!DNL Adobe Connect].

## Adición de co-hosts y presentadores {#add-co-hosts-and-presenters}

1. En la página del seminario web, vaya a la sección **Equipo del seminario web**.

1. Haga clic en **Agregar co-host** o en **Agregar moderador**.

1. En el cuadro de diálogo, escriba el **[!UICONTROL Nombre]**, **[!UICONTROL Apellidos]** y **[!UICONTROL Dirección de correo electrónico]** de la persona y, a continuación, haga clic en **[!UICONTROL Agregar]**.

   >[!NOTE]
   >
   >En la versión actual, todos se agregan de la misma manera, por nombre y correo electrónico, tengan o no una cuenta SSO de Adobe. Vea [Permisos](webinars-overview.md#permissions) para saber qué rigen las funciones de **co-anfitrión del seminario web** y **presentador del seminario web** una vez que se agrega a alguien.

   Una vez agregada la persona, aparecerá una confirmación y aparecerá en la sección **Co-hosts** o **Presentadores** del equipo del seminario web.

## Prueba del seminario web {#test-the-webinar}

Antes de promocionar el seminario web, ejecute una sesión de prueba para confirmar que la sala, los pods y el presentador acceden a todos los roles según lo esperado.

>[!NOTE]
>
>El modo de prueba no afecta al estado de miembro del seminario web de ninguna persona. Puede ejecutar una prueba tantas veces como necesite sin registrar ni invitar a nadie.

## Editar un seminario web en directo {#edit-a-live-webinar}

Puede editar un seminario web después de iniciar los registros, pero hágalo con cuidado:

- La edición de la programación puede almacenar en déclencheur las notificaciones de actualización para personas ya registradas. Se puede configurar la capacidad de editar seminarios web programados.
- Los campos a los que hacen referencia los tokens en correos electrónicos activos requieren una confirmación explícita para su eliminación, ya que esto interrumpe el contenido que ya está programado para su envío.
