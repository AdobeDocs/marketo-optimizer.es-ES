---
title: Creación de WhatsApp
description: Cree mensajes de WhatsApp para recorridos de personas mediante plantillas de Meta aprobadas, tokens de personalización y ajustes de entrega en Marketo Optimizer.
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: 801
ht-degree: 1%

---

# Creación de WhatsApp

Usa [!DNL Adobe Marketo Optimizer] para enviar mensajes de WhatsApp a las personas que usen sus dispositivos móviles. Puede crear, personalizar y previsualizar mensajes utilizando plantillas de mensaje de Meta aprobadas desde el editor de WhatsApp.

Antes de crear mensajes de WhatsApp para recorridos de personas, asegúrate de que tienes un [canal de WhatsApp configurado](../admin/configuration-channels-whatsapp.md) en la configuración de _[!UICONTROL Administrador]_.

>[!NOTE]
>
>Solo se admiten _elementos de mensaje de WhatsApp de salida_ en [!DNL Marketo Optimizer].

+++ Elementos de mensajes compatibles y opciones de call-to-action

Utilice las tablas de esta sección como referencia para el contenido de WhatsApp saliente que puede incluir en plantillas de Meta aprobadas y para los botones interactivos que puede añadir a mensajes.

La siguiente tabla resume los elementos de mensaje admitidos y sus requisitos.

| Elemento de mensaje | Descripción |
| - | - |
| Encabezados | Texto opcional que aparece encima del cuerpo del mensaje. |
| Texto | Admite contenido dinámico mediante parámetros. |
| Imágenes (JPEG, PNG) | Debe tener un formato RGB o RGBA de 8 bits y un tamaño inferior a 5 MB. |
| Vídeos | Debe ser 3GPP o MP4, de menos de 16 MB y alojado por una dirección URL. |
| Audio | Solo disponible para mensajes de respuesta. Debe tener el formato AAC, AMR, MP3, MP4 audio u OGG, alojado en una dirección URL y inferior a 16 MB. |
| Documentos | Debe tener menos de 100 MB, estar alojado en una dirección URL y tener uno de los siguientes formatos: `.txt`, `.xls`/`.xlsx`, `.doc`/`.docx`, `.ppt`/`.pptx` o `.pdf`. |
| Texto independiente | Admite contenido dinámico mediante parámetros. |
| Texto del pie | Admite contenido dinámico mediante parámetros. |

En la tabla siguiente se enumeran los tipos de botones de call-to-action y cómo se comporta cada uno en el mensaje.

| Call to action | Descripción |
| - | - |
| Visitar sitio web | Solo se permite un botón, con parámetros de variable incluidos. |
| Llamar en WhatsApp | Proporciona un botón que abre un chat de WhatsApp con el número de teléfono especificado directamente desde el mensaje. |
| Número de teléfono de llamada | Proporciona un botón que inicia una llamada telefónica al número especificado cuando el usuario lo pulsa. |

+++

## Añadir una acción de WhatsApp en el recorrido de una persona {#add-whatsapp-journey-action}

>[!IMPORTANT]
>
>**Administración de consentimientos de WhatsApp**: De acuerdo con las políticas de Meta y las regulaciones aplicables, todos los mensajes de marketing de WhatsApp deben enviarse únicamente a los destinatarios que se hayan suscrito para recibir comunicaciones. Los destinatarios de WhatsApp pueden excluirse en cualquier momento respondiendo con una palabra clave de exclusión. Las respuestas de exclusión se respetan automáticamente y los perfiles correspondientes se eliminan de las futuras audiencias de mensajes de marketing.

Puedes configurar los envíos de mensajes de WhatsApp en un recorrido de personas cuando [agregues un nodo _[!UICONTROL Realizar una acción]_](../marketing/action-nodes.md) y elegir **[!UICONTROL Enviar WhatsApp]** de la lista de acciones.

## Creación del mensaje de WhatsApp {#create-whatsapp-message}

1. En la parte inferior del panel _[!UICONTROL Realizar una acción]_, haz clic en **[!UICONTROL Crear WhatsApp]**.

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** único (obligatorio) y **[!UICONTROL Descripción]** (opcional) para el mensaje de WhatsApp.

   ![Crear nuevo diálogo de mensaje de WhatsApp](assets/whatsapp-create-dialog.png){width="400"}

1. Haga clic en **[!UICONTROL Crear]**.

   Se abre el _espacio de diseño de WhatsApp_, donde puedes definir las acciones de WhatsApp y crear el contenido para enviar el mensaje.

### Seleccione la configuración de acciones {#select-actions-configuration}

1. En el _espacio de diseño de WhatsApp_, selecciona la pestaña **[!UICONTROL Acciones]**.

1. Para la **[!UICONTROL configuración de WhatsApp]**, selecciona la configuración que admite las acciones de marketing y la configuración de envío de mensajes según tus necesidades.

   ![Crear WhatsApp: ficha Acciones](assets/whatsapp-create-actions-tab.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Editar contenido]** para continuar con los parámetros y el texto del mensaje.

### Seleccione una plantilla de mensaje {#select-message-template}

Los mensajes de WhatsApp se envían utilizando plantillas de mensaje aprobadas previamente desde su cuenta de Meta WhatsApp Business. **Meta debe revisar y aprobar las plantillas** para poder usarlas en [!DNL Marketo Optimizer]. Para administrar y enviar plantillas para su aprobación, comuníquese con el administrador de cuentas de [!DNL Meta Business Manager].

1. Para **[!UICONTROL Seleccionar categoría de plantilla]**, elija una de las siguientes opciones:

   * Marketing
   * Utilidad
   * Autenticación

1. Para **[!UICONTROL Seleccionar plantilla de WhatsApp]**, elige una plantilla aprobada para la cuenta comercial configurada.

   El contenido de la plantilla se carga en el editor de mensajes, mostrando la estructura de la plantilla y los campos de variables disponibles para la personalización.

   ![Plantilla de mensaje de WhatsApp seleccionada con mensaje cargado en la ventana de vista previa](assets/whatsapp-create-select-template.png){width="700" zoomable="yes"}

   El sistema organiza las plantillas por categoría (_Marketing_, _Utilidad_ y _Autenticación_) y estado. Solo hay **_plantillas aprobadas_** disponibles para su selección. Para obtener más información sobre cómo crear plantillas de WhatsApp, consulta [_Crear plantillas de mensajes para tu cuenta de WhatsApp Business_](https://www.facebook.com/business/help/2055875911147364?id=2129163877102343) en la documentación de Meta.

### URL de imagen {#image-urls}

Si la plantilla incluye imágenes, use el campo **[!UICONTROL URL de imagen]** para agregar URL de medios y reemplazar los marcadores de posición en la plantilla. Los medios de plantilla de Meta solo son marcadores de posición. Para mostrar imágenes, audio o vídeo correctamente, debe utilizar direcciones URL externas de Adobe Experience Manager u otras fuentes.

### Personalización del contenido del mensaje {#personalize-message-content}

Las plantillas de WhatsApp aprobadas pueden incluir marcadores de posición variables que se definen con datos de perfil o valores dinámicos.

Para cada campo de variable mostrado en la plantilla, haga clic en el icono _Personalizar_ ( ![Personalizar icono](../assets/do-not-localize/icon-personalize.svg) ) junto al campo.

![Variables en la plantilla de WhatsApp](assets/whatsapp-create-variables.png){width="700" zoomable="yes"}

El cuadro de diálogo proporciona acceso a los tokens de persona y de sistema. Se incluyen tokens estándar y personalizados. Puede usar la barra _Buscar_ para encontrar el token que necesita, o navegar por el árbol de carpetas para buscar y seleccionar cualquiera de los tokens.

Cuando se definan los tokens de personalización, haz clic en **[!UICONTROL Guardar]** para guardar los cambios y volver al área de trabajo principal de mensajes de WhatsApp.
