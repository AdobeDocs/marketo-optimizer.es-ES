---
title: Administración de la privacidad
description: Obtenga información sobre cómo cumplir con el RGPD, la CCPA y otras normas de privacidad en Marketo Optimizer, y enviar solicitudes mediante Adobe Privacy Service.
feature: Setup
role: Admin
TQID: 'https://experienceleague.adobe.com/VgnMCjm6l4pWG2-gqMuOmZUqU7E2Wrc-eVxn4kL5rKc'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 18a33a66-85a1-58e4-8e50-418b832ade8bid: 3cf5f37e-e87e-5179-812b-53ce05d7eebb
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 630
ht-degree: 5%

---


# Administración de la privacidad {#privacy-management}

[Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/es/docs/experience-platform/privacy/home){target="_blank"} proporciona una API RESTful y una interfaz de usuario para ayudarle a administrar las solicitudes de datos de los clientes. Con [!DNL Adobe Privacy Service], puede enviar solicitudes para acceder a datos personales de clientes y eliminarlos de aplicaciones empresariales de Adobe CX, lo que facilita el cumplimiento automatizado de las regulaciones de privacidad legales y organizativas.

[!DNL Adobe Marketo Optimizer] proporciona estas herramientas de privacidad para que pueda cumplir con los requisitos globales de protección de datos. Use [!DNL Privacy Service] para enviar y administrar solicitudes de acceso y eliminación de datos que [!DNL Marketo Optimizer] recopila y almacena.

Puede enviar solicitudes individuales para acceder a los datos de consumidores y eliminarlos de [!DNL Adobe Marketo Optimizer] de dos maneras:

* Interfaz de usuario de [!DNL Privacy Service]
* La API [!DNL Privacy Service]

## Regulaciones de privacidad compatibles {#regulations}

[!DNL Marketo Optimizer] herramientas de privacidad le ayudan a cumplir con las regulaciones a través de [!DNL Privacy Service]. Cada regulación se aplica si se mantienen datos de personas que residen en la región asociada.

Para obtener una lista actualizada de las regulaciones admitidas, consulte [_Resumen de las regulaciones de privacidad_](https://experienceleague.adobe.com/es/docs/experience-platform/privacy/regulations/overview){target="_blank"} en la documentación de Privacy Service.

## Tipos de solicitud {#access-and-delete-requests}

[!DNL Marketo Optimizer] admite dos tipos de solicitud de privacidad:

* **Acceso a datos**: Una persona puede solicitar confirmación de que sus datos personales se están procesando y recibir una copia electrónica gratuita de esos datos.
* **Eliminación de datos** - También se denomina _derecho al olvido_. Una persona puede solicitar que borre sus datos personales y que detenga el procesamiento posterior.

## Visualización y administración de solicitudes de privacidad {#view-manage-requests}

>[!BEGINSHADEBOX]

![Icono de permisos de AEP](../assets/do-not-localize/icon_permissions-outline.svg): estos pasos requieren el perfil de producto [!DNL Privacy Service] y los siguientes [permisos para la función de usuario asignada en Experience Platform](../start/user-management.md#permissions):

* **[!UICONTROL Permisos de Privacy Service]** - `Privacy Read Permission` y `Privacy Write Permission`
* **[!UICONTROL Control de datos]** - `View Privacy Console`

Consulte [_Administrar permisos para Privacy Service_](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/permissions){target="_blank"} en la guía [!DNL Privacy Service] para obtener información más detallada.

>[!ENDSHADEBOX]

Para ver los trabajos de solicitud de privacidad en [!DNL Marketo Optimizer], expanda **[!UICONTROL Privacidad]** y seleccione **[!UICONTROL Solicitudes]**.

Utilice la opción **[!UICONTROL Tipo de regulación]** de la parte superior derecha para cambiar la página mostrada para la regulación que desea que administre trabajos o envíe solicitudes.

![Trabajos de solicitud de privacidad, seleccione el tipo de regulación](./assets/privacy-requests.png){width="800" zoomable="yes"}

### Envío de una solicitud {#submit-a-request}

1. Haga clic en **[!UICONTROL Crear solicitud]**.

1. Para **[!UICONTROL Tipo de trabajo]**, seleccione el tipo de solicitud:

   * **[!UICONTROL Acceso]**

     Cuando envía una solicitud **_access_** que incluye [!DNL Marketo Optimizer], [!DNL Privacy Service] devuelve:

     * [!DNL Marketo Engage] actividad asociada con el posible cliente.
     * [!DNL Marketo Optimizer] actividad asociada con la persona o cuenta.

   * **[!UICONTROL Eliminar]**

     Cuando envía una solicitud **delete** para [!DNL Marketo Engage] y [!DNL Marketo Optimizer], se eliminan los siguientes registros:

     * El posible cliente asociado en [!DNL Marketo Engage].
     * Registros de persona y cuenta creados en [!DNL Marketo Optimizer].
     * Historial de conversaciones con compañeros de trabajo que hace referencia a la información personal de la persona.

1. Para **[!UICONTROL Productos]**, seleccione **[!UICONTROL Marketo]**.

   ![Crear una solicitud de privacidad de acceso de RGPD para Marketo Engage y Marketo Optimizer](./assets/privacy-request-create-gdpr.png){width="450" zoomable="yes"}

   Esta selección incluye datos de [!DNL Marketo Optimizer] y de su instancia [!DNL Marketo Engage].

1. Desplácese hasta la parte inferior del cuadro de diálogo e introduzca la dirección de correo electrónico de la persona a cuyos datos desea acceder o eliminar.

1. Para enviar la solicitud, haga clic en **[!UICONTROL Crear]**.

   [!DNL Privacy Service] devuelve un ID de solicitud que puede usar para comprobar el estado de su solicitud.

### Solicitudes de API {#api-requests}

También puede enviar solicitudes de privacidad mediante la API [!DNL Privacy Service]. Para obtener una referencia general de la API, consulte la [Documentación de la API de Privacy Service](https://developer.adobe.com/experience-platform-apis/references/privacy-service){target="_blank"}.

>[!PREREQUISITES]
>
>Recopile la siguiente información antes de enviar una solicitud:
>
>* El identificador de organización de IMS de su organización (una cadena alfanumérica de 24 caracteres que termina en `@AdobeOrg`). Póngase en contacto con el Soporte técnico de Adobe en `gdprsupport@adobe.com` si no conoce su ID de organización de IMS.
>* La dirección de correo electrónico de la persona a cuyos datos desea acceder o eliminar.

Utilice los siguientes valores de campo en la solicitud:

| Campo | Valor |
|---|---|
| `companyContexts.namespace` | `imsOrgID` |
| `companyContexts.value` | Su ID de organización de IMS |
| `users.action` | `access` o `delete` |
| `users.userIDs.namespace` | `Email` |
| `include` | `marketo` para incluir datos de [!DNL Marketo Optimizer] y [!DNL Marketo Engage] |
| `regulation` | Ejemplo: `ccpa` <br/>Algunos valores de regulación están cambiando para incluir una abreviatura de estado (por ejemplo, `ucpa_ut_usa`). Los valores anteriores siguen siendo válidos durante un periodo de transición. Consulte la [descripción general de las regulaciones de privacidad](https://experienceleague.adobe.com/es/docs/experience-platform/privacy/regulations/overview){target="_blank"} para ver la lista actual antes de generar integraciones con estos valores. |

En el siguiente ejemplo se envía una solicitud de eliminación de RGPD que incluye [!DNL Marketo Optimizer] datos.

```json
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "1231659F56A68A8B7F000101@AdobeOrg"
    }
  ],
  "users": [
    {
      "action": ["delete"],
      "userIDs": [
        {
          "namespace": "Email",
          "type": "standard",
          "value": "john.doe@adobe.com"
        }
      ]
    }
  ],
  "include": ["marketo"],
  "regulation": "gdpr"
}
```

[!DNL Privacy Service] devuelve una respuesta similar a la siguiente.

```json
{
  "requestId": "16331241037112570RX-245",
  "totalRecords": 1,
  "jobs": [
    {
      "jobId": "997b01e3-9568-402c-904b-b4e60a437875",
      "customer": {
        "user": {
          "action": ["delete"],
          "userIDs": [
            {
              "namespace": "Email",
              "value": "john.doe@adobe.com",
              "type": "standard",
              "namespaceId": 6,
              "isDeletedClientSide": false
            }
          ]
        }
      }
    }
  ]
}
```
