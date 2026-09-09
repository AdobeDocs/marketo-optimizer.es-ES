---
title: Crear plantillas de correo electrónico
description: 'Obtenga información sobre cómo crear plantillas de correo electrónico en Marketo Optimizer: crear nuevas plantillas, guardar un correo electrónico de un recorrido como plantilla o convertir una imagen de diseño en una plantilla de correo electrónico.'
TQID: 'https://experienceleague.adobe.com/Hag-o6Hu-82rqnWHnDBgPD-dKApy5JGsPMD5cGFOCfA'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 8881ff95-1653-5fea-82af-ce1549c0d99d
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 873
ht-degree: 1%

---


# Crear plantillas de correo electrónico

Puede crear una plantilla de correo electrónico en [!DNL Adobe Marketo Optimizer] de tres maneras:

* **Crear una nueva plantilla**: cree una plantilla en la biblioteca de plantillas con el espacio de diseño de correo electrónico visual.
* **Guardar desde un correo electrónico de recorrido**: guarde un correo electrónico que haya creado en un recorrido como una plantilla reutilizable.
* **Convertir una imagen**: cargue una imagen de diseño y use IA generativa para convertirla en una plantilla de correo electrónico editable.

## Crear una plantilla nueva {#build-new}

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Administración de contenido]** y seleccione **[!UICONTROL Plantillas]**.
1. Haga clic en **[!UICONTROL Crear plantilla]**.
1. Escriba un **[!UICONTROL nombre de plantilla]** y una **[!UICONTROL descripción]** opcional.
1. Establezca el **[!UICONTROL canal]** (tipo) para la plantilla.

   >[!NOTE]
   >
   >En esta versión de Beta, solo se admiten plantillas de correo electrónico.

   <!-- 1. Optionally add **[!UICONTROL Tags]** to categorize the template. -->

1. Haga clic en **[!UICONTROL Crear]** para abrir el espacio de diseño de correo electrónico.

1. Haga clic en **[!UICONTROL Editar cuerpo del correo electrónico]** para acceder al espacio de diseño de contenido.

   Consulte [Creación de correo electrónico](email-authoring.md) para obtener información detallada sobre el diseño de contenido.

1. De forma opcional, habilite **[!UICONTROL Governance]** y configure [el bloqueo de contenido](template-content-governance.md) para restringir qué partes de los autores de plantillas pueden editar al aplicar la plantilla.

1. Haga clic en **[!UICONTROL Guardar]**.

## Guardar un correo electrónico como plantilla {#save-as-template}

Cuando abra el contenido del correo electrónico que desea reutilizar, guárdelo directamente en la biblioteca de plantillas desde la página de contenido del correo electrónico.

1. Haga clic en **[!UICONTROL Plantilla de contenido]** en la parte superior de la página.
1. Seleccione **[!UICONTROL Guardar como plantilla de contenido]**.
1. Escriba un **[!UICONTROL Nombre]** y una **[!UICONTROL Descripción]** opcional.
1. Opcionalmente, agregue **[!UICONTROL Etiquetas]**.
1. Haga clic en **[!UICONTROL Crear]**.

El correo electrónico de recorrido original no se ve afectado. La plantilla guardada está disponible en la biblioteca de plantillas para todos los usuarios de la zona protegida. Puede actualizar la plantilla creada para optimizar su reutilización:

* Edite texto y agregue [tokens de personalización](email-authoring.md#personalize-content).
* Actualizar o reemplazar imágenes y agregar vínculos.
* Configurar [bloqueo de contenido](template-content-governance.md).

## Convertir una imagen en una plantilla {#image-to-template}

[!DNL Adobe Marketo Optimizer] puede convertir una imagen estática, como una maqueta de Figma o Photoshop, en una plantilla de correo electrónico editable mediante IA generativa. Esto elimina la necesidad de reconstruir manualmente los diseños a partir de archivos de diseño y es ideal para migrar los diseños de correo electrónico existentes desde otras plataformas. Esta función solo está disponible para plantillas de contenido de correo electrónico.

>[!BEGINSHADEBOX]

### Requisitos previos

Antes de empezar:

* Su organización debe haber firmado el anexo de IA generativa con Adobe.
* Debe tener el permiso **[!UICONTROL Generar contenido]** además de **[!UICONTROL Administrar plantillas de contenido]**.
* El archivo de imagen debe cumplir estas especificaciones:
  * Formato: JPEG (.jpg, .jpeg) o PNG (.png)
  * Tamaño máximo de archivo: 10 MB
  * Anchura recomendada: 600-800 píxeles
  * Imagen clara y de alta calidad con texto legible y distintos elementos visuales

>[!IMPORTANT]
>
>La imagen no debe contener información de identificación personal (PII) ni datos confidenciales.

>[!ENDSHADEBOX]

### Creación de la plantilla

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Administración de contenido]** y seleccione **[!UICONTROL Plantillas]**.
1. Haga clic en **[!UICONTROL Crear plantilla]**.
1. Escriba un **[!UICONTROL nombre de plantilla]** y una **[!UICONTROL descripción]** opcional.
1. Establece el **[!UICONTROL canal]** en correo electrónico.

   <!--  Optionally add **[!UICONTROL Tags]** to categorize the template. -->

1. Haga clic en **[!UICONTROL Crear]**.

### Generación del contenido de la plantilla

1. En la sección **[!UICONTROL Convertir imagen en plantilla]**:

   * Si lo desea, seleccione **[!UICONTROL Tema de marca]** para aplicar los colores, las fuentes y el espaciado de su marca a la salida generada.
   * Seleccione la casilla de verificación de confirmación para confirmar que la imagen no contiene información de identificación personal (PII) u otros datos confidenciales.
   * Haga clic en **[!UICONTROL Cargar imagen]** y seleccione el archivo de imagen.

   >[!CAUTION]
   >
   >Al cargar una imagen, se elimina cualquier contenido que esté actualmente en el correo electrónico y se sustituye por la plantilla generada.

1. Si se le solicita, revise y acepte las Directrices del usuario de IA generativa de Adobe.

1. Haga clic en **[!UICONTROL Abrir]** para iniciar el proceso de conversión.

   La conversión suele completarse en unos cinco minutos. Las imágenes complejas o grandes pueden tardar hasta diez minutos. La conversión se ejecuta en segundo plano: puede salir y la plantilla de borrador se guarda automáticamente cuando se completa la conversión.

1. Actualice la página para ver la plantilla completada.

   >[!NOTE]
   >
   >El resultado no se muestra automáticamente. Actualice la página o vuelva a la biblioteca de plantillas para ver la plantilla completada.

1. De manera opcional, usa la sección **[!UICONTROL comentarios del convertidor de imágenes a plantillas]** para compartir sugerencias con Adobe.

1. Haga clic en **[!UICONTROL Editar cuerpo del correo electrónico]** para abrir la plantilla convertida en el espacio de diseño del correo electrónico y editarla.

1. Haga clic en **[!UICONTROL Guardar]**.

### Editar el contenido convertido

El contenido de plantilla convertido se abre en el espacio de diseño como una plantilla de correo electrónico totalmente editable. Utilice las herramientas de diseño de contenido estándar para lo siguiente:

* Edite texto y agregue [tokens de personalización](email-authoring.md#personalize-content).
* Actualizar o reemplazar imágenes y agregar vínculos.
* Ajustar colores, fuentes y espaciado.
* Agregar, quitar o reorganizar componentes de contenido.
* Habilite el control y configure el [bloqueo de contenido](template-content-governance.md).

>[!IMPORTANT]
>
>La IA generativa produce una HTML estática basada en la imagen visual. Revise todo el texto para comprobar su precisión y agregue personalización, contenido dinámico y seguimiento manualmente después de la conversión.

La plantilla convertida se guarda automáticamente en la biblioteca de plantillas cuando se completa la conversión.

### Sugerencias para obtener mejores resultados

Siga estas directrices para obtener los mejores resultados de la conversión de imagen a plantilla:

**Antes de la conversión:**

* Utilice la versión de mayor resolución del archivo de diseño.
* Diseñe con anchuras de correo electrónico estándar (600-800 píxeles) e incluya el diseño completo (de encabezado a pie de página) en una sola imagen.
* Asegúrese de que haya suficiente contraste entre el texto y los fondos y utilice tamaños de fuente legibles.

**Diseño para una conversión precisa:**

* Utilice diseños sencillos y bien estructurados con una clara separación entre las secciones.
* Siga los patrones de correo electrónico estándar (encabezado, cuerpo, llamadas a la acción, pie de página) en lugar de diseños complejos de varias capas.
* Mantenga los elementos visuales distintos para que la IA pueda identificar correctamente los límites estructurales.

**Después de la conversión:**

* Pruebe el procesamiento en clientes de correo electrónico y dispositivos antes de utilizar la plantilla en un recorrido.
* Compruebe la alineación con los colores de marca, las fuentes y las directrices de estilo.
* Revise y mejore la accesibilidad, incluido el texto alternativo de la imagen.
