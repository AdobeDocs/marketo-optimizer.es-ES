---
title: Configuración del canal de correo electrónico
description: Cree y administre configuraciones de canal de correo electrónico que enlacen la identidad del remitente, el subdominio, el grupo de IP, el tipo de correo electrónico y el seguimiento de URL para Marketo Optimizer.
feature: Administration
role: Admin
TQID: 'https://experienceleague.adobe.com/VDqL3u2vPJ8YGJgZCx5lE0Xt1-WvAEBBwFiMZGj7w90'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2:
  - id: 3cf5f37e-e87e-5179-812b-53ce05d7eebb
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
  - id: a659ad61-de21-559d-a901-02e2fb329ff5
  - id: d4203578-d294-5145-b397-f26f4488a904
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 624
ht-degree: 0%

---

# Configuración de canal de correo electrónico

Una configuración de canal es el objeto central que vincula la identidad del remitente, el subdominio, el grupo de IP y la configuración de seguimiento. Las acciones de correo electrónico en los recorridos hacen referencia a una configuración de canal para saber cómo enviar el mensaje. Antes de crear una configuración, complete la [delegación de subdominios y la configuración del grupo de IP](../start/email-deliverability.md).

* **Canal:** Correo electrónico.
* **Tipo de correo electrónico:** Marketing o transaccional. Esta configuración determina si se aplican las reglas de supresión (Marketing las aplica; Transactional omite la supresión de quejas de spam de forma predeterminada para los mensajes transaccionales legítimos).
* **Parámetros De Encabezado:** Del Nombre, Del Correo Electrónico, Del Nombre De Respuesta, Del Correo Electrónico De Respuesta, Del Correo Electrónico De Error.
* **Subdominio:** El subdominio delegado utilizado para el envío. El correo electrónico de origen debe utilizar este subdominio.
* **Grupo de IP:** Grupo de IP usado para entregar el mensaje.
* **Seguimiento de URL:** Habilite o deshabilite el rastreo de clics y aperturas; configure el dominio de seguimiento.
* **Etiquetas:** Etiquetas para organización y búsqueda.

## Crear una configuración de canal de correo electrónico {#create-email-channel-configuration}

>[!PREREQUISITES]
>
>* Al menos un [subdominio](../start/email-deliverability.md#subdomain-delegation) debe estar delegado y activo.
>* Se debe asignar al menos un [grupo de IP](../start/email-deliverability.md#ip-pools) a su organización.
>* Necesita la función Administrador.
>* Revise [las limitaciones actuales](../start/email-deliverability.md#limitations): los grupos de IP dedicados no están disponibles en Beta.

1. En la navegación izquierda de [!DNL Adobe Marketo Optimizer], expanda **[!UICONTROL Administración]** y seleccione **[!UICONTROL Canales]**.
1. En el panel, expanda **[!UICONTROL Configuración de correo electrónico]** y seleccione **[!UICONTROL Configuraciones de canal]**.
1. Haga clic en **[!UICONTROL Crear configuración de canal]**.
1. Escriba un Nombre (por ejemplo, _Contoso B2B Marketing — Norteamérica_) y una Descripción opcional.
1. Seleccione el canal **[!UICONTROL Correo electrónico]**.
1. (Opcional) Seleccione etiquetas para categorizar la configuración.
1. En la sección **[!UICONTROL Tipo de correo electrónico]**, elija Marketing o Transaccional.
1. En la sección **[!UICONTROL Subdominio]**, seleccione un subdominio delegado anteriormente.
1. En la sección **[!UICONTROL grupo de IP]**, seleccione un grupo de IP activo.

   En Beta, solo está disponible el grupo de IP compartidas. Puede pasar el ratón sobre las direcciones IP para ver los registros PTR.

1. Configurar los **[!UICONTROL parámetros de encabezado]**:
   * Nombre de origen (por ejemplo, &quot;Contoso Marketing&quot;).
   * Desde correo electrónico: debe utilizar el subdominio seleccionado (por ejemplo, `marketing@mail.contoso.com`).
   * Nombre de respuesta y correo electrónico de respuesta: si está en blanco, el valor predeterminado es _De_.
   * Correo electrónico de error: dirección que recibe notificaciones de no entrega.
1. Habilite **[!UICONTROL Seguimiento de URL]** y seleccione el dominio de seguimiento.
1. Haga clic en **[!UICONTROL Enviar]**.

>[!NOTE]
>
>Después de enviar, el sistema ejecuta la validación: estado de subdominio, registro MX, alineación SPF/DKIM/DMARC, preparación del grupo de IP, registro FBL. La configuración se desplaza por Borrador → Procesamiento → Activo.

>[!NOTE]
>
>Si la validación falla, la configuración pasa al estado **[!UICONTROL Failed]**. Abra la configuración para ver el motivo del error: las causas comunes son un error de validación de registro MX, IP en el grupo que no coinciden con la configuración o desalineación de DMARC. Resolver y volver a enviar.

## Editar o eliminar una configuración de canal {#edit-channel-configuration}

Puede editar las configuraciones de canal después de la creación, pero con una restricción importante: **El canal no se puede cambiar.** Una configuración de está enlazada a su canal.

Cuando edita una configuración que está en uso:

* **Para recorridos publicados:** el cambio se aplica en la siguiente periodicidad o en la siguiente ejecución. Las ejecuciones en vuelo continúan con la configuración anterior.
* **Para mensajes transaccionales o en tiempo real:** cambios se propagan en unos cinco minutos.

>[!WARNING]
>
>La eliminación de una configuración de canal es permanente. No puede eliminar una configuración a la que haga referencia un recorrido activo. Elimine o reasigne primero todas las acciones de correo electrónico.

Para eliminar una configuración, primero quita o actualiza cada acción de correo electrónico que haga referencia a ella en [Agregar correos electrónicos a recorridos](../marketing/email-channel.md#define-email-properties). [!DNL Marketo Optimizer] no elimina una configuración que esté siendo utilizada actualmente por un recorrido activo.

## Configuraciones de varios canales {#multiple-channel-configurations}

La mayoría de las organizaciones B2B utilizan varias configuraciones de canal para separar marcas, regiones o tipos de envío. Patrones comunes:

* Una configuración de marketing independiente por unidad de negocio (por ejemplo, *Marketing BU-A*, *Marketing BU-B*).
* Una configuración transaccional dedicada con Tipo de correo electrónico = Transaccional para las notificaciones de productos o contratos.
* Configuraciones específicas de la región que utilizan subdominios específicos de la región (por ejemplo, `mail.eu.contoso.com`, `mail.us.contoso.com`) para alinearse con los ISP regionales y el cumplimiento.

>[!TIP]
>
>Asigne un nombre a las configuraciones con una convención clara y estructurada, por ejemplo: *[Marca] - [Región] - [Tipo]*. Esto resulta esencial una vez que tenga una docena o más de configuraciones.
