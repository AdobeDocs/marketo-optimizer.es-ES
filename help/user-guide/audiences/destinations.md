---
title: Destinos
description: Obtenga información acerca de los permisos necesarios, los destinos admitidos y cómo conectar un destino en Marketo Optimizer para activar listas de personas estáticas en plataformas publicitarias y sociales.
TQID: 'https://experienceleague.adobe.com/u5sWVDR0JaiX-YvlQ23l7mqoI9G95xS-uiKcqANwsnc'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2:
  - id: 3cf5f37e-e87e-5179-812b-53ce05d7eebb
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 643
ht-degree: 7%

---

# Destinos

Los destinos son integraciones prediseñadas que le permiten enviar [listas de personas estáticas](./people-lists.md#static-lists) desde [!DNL Marketo Optimizer] a publicidad externa o plataformas sociales, como una audiencia de campaña de LinkedIn, una audiencia de Customer Match de Google o una audiencia personalizada de Facebook. La activación de una lista estática en un destino mantiene la pertenencia sincronizada: a medida que se añaden personas a la lista o se eliminan de ella, estas se añaden o eliminan en consecuencia de la audiencia de destino y, por extensión, de cualquier campaña a la que la audiencia alimente.

Existen dos formas de activar personas en un destino conectado:

* **De una lista estática**: active una lista estática existente directamente desde la ficha **_[!UICONTROL Listas de personas]_**. Ver [Activar en un destino](./people-lists.md#static-list-activate).
* **De un recorrido de persona**: agregue una acción **_[!UICONTROL Activar en destino]_** a una ruta de acceso de recorrido para que cualquier persona que llegue a ese nodo se agregue a una lista y se envíe al destino. Consulte [_Agregar un nodo de acción_](../marketing/action-nodes.md#add-an-action-node).

>[!BEGINSHADEBOX]

## Permisos necesarios {#required-permissions}

La funcionalidad de destino completa requiere que se habiliten los siguientes [!DNL Adobe Experience Platform] permisos.

| Categoría | Permiso | Requerido |
|--- |--- |--- |
| Zonas protegidas | Acceso a zona protegida _(habilitado de forma predeterminada)_ | Sí |
| Paneles de control | Ver paneles estándar | Sí |
| Paneles de control | Administrar paneles estándar | Sí |
| Destinos | Ver destinos | Sí |
| Destinos | Administrar destinos | Sí |
| Destinos | Activar destinos | Sí |
| Destinos | Activar segmento sin asignación | Sí |
| Destinos | Administrar y activar el destino del conjunto de datos | Sí |
| Destinos | Creación de destino | Sí |
| Gobernanza de datos | Ver directivas de uso de datos | Sí |
| Gobernanza de datos | Administrar políticas de uso de datos | Sí |
| Ingesta de datos | Ver orígenes | Sí |
| Ingesta de datos | Administrar fuentes | Sí |
| Administración de perfiles | Ver configuración del perfil | Sí |
| Administración de perfiles | Administrar configuración de perfil | Sí |

>[!ENDSHADEBOX]

## Destinos admitidos {#supported-destinations}

Para poder activar una lista estática, debe existir un destino en el catálogo de destinos. En el panel de navegación izquierdo, expanda **[!UICONTROL Conexiones]** y seleccione **[!UICONTROL Destinos]**. [!DNL Marketo Optimizer] admite actualmente los siguientes destinos:

* **[!UICONTROL Coincidencia de clientes de Google]** (Advertising)
* **[!UICONTROL Audiencia personalizada de Facebook]** (Social)
* **[!UICONTROL Audiencia coincidente de LinkedIn]** (Social)

![Acceder a los tipos de conectores disponibles](./assets/destinations-catalog.png){width="800" zoomable="yes"}

>[!NOTE]
>
>Este catálogo no es el catálogo de destinos completo de [!DNL Adobe Experience Platform]. Si accede a destinos directamente desde [!DNL Experience Platform], verá un catálogo más grande, pero solo estos destinos están disponibles actualmente para su activación en [!DNL Marketo Optimizer]. Hay destinos adicionales planificados para futuras versiones.

## Configurar un destino {#set-up-destination}

Cada tarjeta de destino admitida muestra **[!UICONTROL Configurar nuevo destino]**. La configuración de un destino es un requisito previo para la activación.

1. En la tarjeta del conector, haga clic en **[!UICONTROL Configurar nuevo destino]**.

1. Seleccione **[!UICONTROL Cuenta existente]** o **[!UICONTROL Cuenta nueva]** e introduzca los detalles de la cuenta, como el nombre y la descripción de la cuenta.

   ![Conectar una nueva cuenta de destino](./assets/destinations-configure-new.png){width="500"}

1. Haga clic en **[!UICONTROL Conectar con destino]**.

   Un flujo de OAuth le permite iniciar sesión en la cuenta correspondiente: LinkedIn, Google o Facebook.

   >[!IMPORTANT]
   >
   >En este momento, **no** escribe los _[!UICONTROL detalles del destino]_. Solo se necesita la conexión.

1. Complete cualquier asignación de campo requerida entre los atributos de las personas y los campos requeridos por el destino.

1. Revise la configuración del control de datos y la acción de marketing y, a continuación, haga clic en **[!UICONTROL Guardar]**.

Para ver los pasos completos de la configuración, consulte [Crear una nueva conexión de destino](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/ui/connect-destination){target="_blank"} en la documentación de [!DNL Experience Platform].

Cuando está configurado, el destino está disponible para la activación en todas partes donde se puede seleccionar un destino en [!DNL Marketo Optimizer].

## Activación y sincronización {#activation-sync}

La activación se basa en la pertenencia a listas estáticas, con una sincronización bidireccional entre la lista y la audiencia de destino:

* Añadir una persona a la lista estática la activa en el destino en un plazo de 24 horas, añadiéndola a la audiencia de destino y, posteriormente, a cualquier campaña que alimente la audiencia.
* Al eliminar a una persona de la lista estática, se desactiva del destino (se elimina de la audiencia de destino y de cualquier campaña conectada).
* La misma lista se puede activar en varios destinos a la vez; la pertenencia se sincroniza con todos ellos.

>[!TIP]
>
>Para ejecutar una campaña de LinkedIn en un segmento, active la lista estática de esas personas en el destino de audiencia coincidente de LinkedIn. Todas las personas de la lista se añaden a la audiencia coincidente de LinkedIn, donde una campaña puede dirigirlos y la audiencia se mantiene actualizada automáticamente a medida que cambia la lista.
