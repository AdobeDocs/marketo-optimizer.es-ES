---
title: Metadatos de C2PA
description: Descubra cómo Adobe Marketo Optimizer aplica automáticamente los metadatos de C2PA a las imágenes generadas con IA generativa y qué significa esto para su contenido.
feature: Assets, Content
role: User
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Metadatos de C2PA

Las organizaciones de marketing están más preocupadas que nunca por la transparencia del contenido, la divulgación de la IA y la prevención de la manipulación de activos. Content Authenticity Initiative (CAI) en Adobe crea herramientas compatibles con el estándar técnico de [Coalición para la procedencia y autenticidad del contenido](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA). Los _metadatos de C2PA_ son información cifrada y a prueba de manipulaciones que puede ayudar a los espectadores a comprender el linaje del contenido y garantizar la integridad de los recursos de la marca. Esta información incluye:

* Emisor o signatario: información sobre la entidad o compañía que emitió la firma digital para certificar o firmar el activo.
* Fecha de emisión: la fecha en la que se aplicaron los metadatos de C2PA al recurso.
* Crédito y uso: información sobre el productor del recurso, incluido el nombre, los identificadores de las redes sociales u otra información relacionada con la identidad.
* Proceso: Registra las ediciones o modificaciones realizadas en el recurso.
* Detalles del dispositivo: información sobre la aplicación o el dispositivo utilizado para crear o editar el recurso.
* Herramienta de IA utilizada: si se ha utilizado IA generativa para crear el recurso, se puede incluir el nombre del modelo utilizado.
* Otra información pertinente: también se incluyen datos adicionales para ayudar a ofrecer más contexto sobre el historial de un recurso.

Para obtener información completa sobre el historial de recursos, puede usar la [herramienta de inspección](https://contentauthenticity.adobe.com/inspect) de Adobe Content Authenticity.

Los metadatos de C2PA persisten con el archivo de imagen. Cuando se carga o exporta una imagen generada o editada con IA generativa desde [!DNL Adobe Marketo Optimizer], se conservan sus metadatos de C2PA.

>[!NOTE]
>
>Es posible que algunos métodos para importar imágenes en el contenido, como extraer una imagen de un PDF o de un origen incrustado (base64), no conserven los metadatos originales de C2PA. En estos casos, los metadatos de C2PA no se pueden leer desde el origen y no se crea ninguno para el resultado.

>[!BEGINSHADEBOX]

## Persistencia de metadatos de C2PA a través de canales {#channels}

Cuando se incluyen imágenes en los mensajes de correo electrónico o WhatsApp, los metadatos de C2PA de las imágenes entregadas también se mantienen:

* **Correo electrónico**: cuando uses una acción de recorrido _Enviar correo electrónico_, agrega la imagen al contenido del correo electrónico desde la biblioteca de _Assets_. Cuando se envía el correo electrónico, el destinatario puede descargar la imagen del mensaje y los metadatos de C2PA están intactos.
* **WhatsApp**: agrega la imagen a la plantilla de mensaje de WhatsApp en tu cuenta comercial de Meta. Puede agregarlo directamente desde el sistema o descargar un archivo de imagen desde la biblioteca _Assets_. Usa la plantilla para una acción de recorrido _Enviar aplicación WhatsApp_. Cuando se envía el mensaje de WhatsApp, el destinatario puede descargar la imagen del mensaje y los metadatos de C2PA están intactos.

>[!ENDSHADEBOX]

## Generación de imágenes {#generate}

>[!INFO]
>
>Están surgiendo nuevas leyes en torno a la transparencia generativa de la IA, y Adobe está trabajando para cumplir con los requisitos aplicables en todas las jurisdicciones. Los metadatos de C2PA son la herramienta de procedencia que utiliza Adobe para cumplir con los requisitos de estas leyes.

Cuando usa IA generativa para crear una imagen para el contenido del correo electrónico en [!DNL Marketo Optimizer], los metadatos de C2PA se adjuntan automáticamente a la imagen generada y no se requiere ninguna acción por su parte. Las herramientas de IA generativa producen un elemento de metadatos C2PA combinado para variantes de imágenes con metadatos existentes, incluido el origen.

>[!NOTE]
>
>[!DNL Marketo Optimizer] no admite actualmente las acciones manuales de edición de imágenes. Los flujos de trabajo de metadatos de C2PA para estas acciones no son aplicables en este momento.
