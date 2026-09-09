---
title: Tipos de programas
description: Cree y administre tipos de programas que definan atributos y flujos de estado de miembros para programas en Marketo Optimizer.
TQID: 'https://experienceleague.adobe.com/Eepcnc51p-P-yoyylXBr47SF0xR-3pvZab2aHf9jdew'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: a29661b8-f7a4-53d1-a9ac-fdec08c092e4id: a659ad61-de21-559d-a901-02e2fb329ff5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 389
ht-degree: 0%

---

# Tipos de programas

Los tipos de programas definen aspectos importantes de [programas](../marketing/programs.md) y sus miembros, y distinguen los distintos tipos de programas de marketing entre sí. Cada tipo de programa define las siguientes propiedades, que se heredan para los programas que utilizan el tipo de programa:

* **Atributos**: los atributos describen aspectos importantes del tipo de programa, como fechas de eventos y atributos de ubicación.

* **Flujo de estado del programa** - Cada estado se asigna a un paso en el tipo de programa (como 1, 2 o 3). Los miembros de un programa solo pueden pasar de un estado con el mismo número de paso (por ejemplo, de _No mostrado_ a _Asistido_) o a un estado con un número de paso superior (por ejemplo, de _Invitado_ a _Registrado_).

  Los estados de los programas son mutuamente excluyentes y lineales, por lo que una persona solo puede tener un valor de estado por programa. Al diseñar estados, piense en los estados entre los que desee permitir el movimiento. Por ejemplo, si alguien no asistió a un seminario web pero tiene la opción de asistir a petición más tarde, le interesa que tenga el mismo número de estado o que establezca un número de estado más alto a petición para que un miembro del programa pueda avanzar a él.

>[!NOTE]
>
>Si al menos un programa utiliza un tipo de programa, no se puede editar.

_Para definir un tipo de programa personalizado :_

1. En la navegación izquierda de [!DNL Adobe Marketo Optimizer], expanda **[!UICONTROL Administración]** y seleccione **[!UICONTROL Tipos de programa]**.

   ![Acceder a la lista de tipos de programas](./assets/program-types-list.png){width="800" zoomable="yes"}

1. Haga clic en **[!UICONTROL Crear tipo]** en la parte superior derecha.

1. Escriba un **[!UICONTROL Nombre]** único (obligatorio) y una **[!UICONTROL Descripción]** (opcional).

   ![Crear tipo de programa](./assets/program-type-create.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >Incluir una descripción es una práctica recomendada y hace que la biblioteca de tipos de programa sea más manejable.

1. Haga clic en **[!UICONTROL Crear tipo]**.

1. Agregue los **[!UICONTROL Atributos]** para el tipo de programa.

   Para cada atributo que desee agregar:

   * Haga clic en **[!UICONTROL Agregar atributo]**.
   * Elija **[!UICONTROL nombre de API]** e introduzca **[!UICONTROL nombre para mostrar]**.
   * Haga clic en **[!UICONTROL Guardar]**.

   ![Atributos de tipo de programa](./assets/program-type-attributes.png){width="600" zoomable="yes"}

1. Defina los pasos para **[!UICONTROL estados de programas]**.

   Defina cada paso que desee incluir en el flujo:

   * Haga clic en **[!UICONTROL Agregar paso]**.
   * Introduzca un nombre de estado.
   * (Opcional) Haga clic en **[!UICONTROL Agregar estado]** e introduzca un nombre de estado adicional para incluir en el paso.

   Active la casilla de verificación **[!UICONTROL Marcar como correcto]** para cualquier paso que desee rastrear como una ejecución correcta del programa.

   ![Estados de tipo de programa](./assets/program-type-statuses.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Listo]** para guardar los cambios y volver a la lista de tipos de programas.