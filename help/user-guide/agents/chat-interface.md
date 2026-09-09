---
title: Interfaz de chat
description: Utilice el panel de chat Compañero de trabajo en Marketo Optimizer para crear programas, recorridos y listas con lenguaje natural o el menú de barra (/).
TQID: 'https://experienceleague.adobe.com/5oj0glKEbJuzQFem-jxL4qjnzxVG4tlOaiHKM5SuiWQ'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 1650dadf-b034-5ac9-a309-77ad1e2f5035id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1id: a29661b8-f7a4-53d1-a9ac-fdec08c092e4id: d4203578-d294-5145-b397-f26f4488a904
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 928
ht-degree: 0%

---

# Interfaz de chat

El panel de chat está incrustado en [!DNL Adobe Marketo Optimizer]. Es donde interactúa con los agentes de IA utilizando un lenguaje sencillo para crear programas y recorridos, crear y comparar listas de personas, investigar posibles clientes, configurar la puntuación y mucho más.

Seleccione el icono _Compañero_ en el panel de navegación izquierdo para abrir el panel. El encabezado del panel tiene cuatro controles:

| Control | Descripción |
|---------|-------------|
| **Nueva conversación** | Iniciar un nuevo chat (borra el hilo actual). |
| **Historial de conversaciones** | Abra las conversaciones anteriores para poder volver a abrir una. |
| **Intercambiar paneles** | Mueva el panel de chat al otro lado del espacio de trabajo. |
| **Contraer** | Oculte el panel para dejar más espacio al espacio de trabajo. |

En la parte inferior del panel se encuentra el cuadro de mensaje, donde puede:

* Agrega un mensaje y presiona **Intro** para enviar (**Mayús+Intro** inserta una nueva línea).
* Adjuntar un archivo mediante el icono _Adjuntar_ (formatos admitidos: `.txt`, `.md`, `.csv`, `.json`, `.xlsx`, `.docx`, `.pdf`). Utilice CSV y cargas de hoja de cálculo para iniciar una importación de posibles clientes.

>[!BEGINSHADEBOX]

## Calificador de ventas

[!DNL Adobe Sales Qualifier] es una aplicación controlada por IA que puede usar con [!DNL Marketo Optimizer]. Implementa Account Qualification Agent y está diseñado para optimizar los flujos de trabajo para los representantes de desarrollo empresarial (BDR). [!DNL Sales Qualifier] automatiza los flujos de trabajo de cualificación de clientes potenciales, alcance y participación del comprador en todos los canales. Reduce la carga manual de BDR y acelera la velocidad de la canalización para las empresas B2B empresariales.

Para obtener más información, consulte la [documentación de Sales Qualifier](https://experienceleague.adobe.com/en/docs/sales-qualifier/using/home){target="_blank"}.

>[!ENDSHADEBOX]

## Preguntar a compañero

Existen dos formas igualmente válidas de realizar el trabajo: nunca es necesario utilizar el menú de barra.

**Lenguaje natural** — Escriba su solicitud de la forma en que se lo diría a un compañero:

* _&quot;Crear un recorrido de bienvenida para nuevos registros de prueba.&quot;_
* _&quot;¿Por qué john@acme.com no entró en este recorrido?&quot;_
* _&quot;Comparar mis listas &#39;Asistentes al seminario web del tercer trimestre&#39; y &#39;Cuentas empresariales&#39;.&quot;_

El agente adapta la redacción a la aptitud correcta entre bastidores y ejecuta el flujo de trabajo adecuado.

**Menú de barra diagonal (/)** — Escriba `/` para abrir un menú explorable de todo lo que el compañero puede hacer. Esto resulta útil cuando desea descubrir funcionalidades o ir directamente a un flujo de trabajo conocido.

## Menú de barra (/)

Use un `/` al principio del cuadro de mensaje o después de un espacio para abrir el menú. A medida que continúa escribiendo, la lista se filtra por nombre, descripción o identificador; por ejemplo, `/journey` se reduce a comandos relacionados con el recorrido.

Use **/** para desplazarse por las entradas, **Escriba** o **Tabulación** para seleccionar y **Esc** para descartar. También puede hacer clic directamente en una entrada.

Las entradas de menú se agrupan en secciones etiquetadas:

| Sección | Contiene |
|---------|----------|
| **Investigar** | Búsquedas de diagnóstico y solo lectura (por ejemplo, investigación de posibles clientes, consultas por intención). |
| **Validar** | Flujos de trabajo de control de calidad y auditoría. |
| **Compilación** | Flujos de trabajo de creación (programas, recorridos, listas, puntuación). |
| **Importar** | Importación de cliente potencial CSV. |
| **Otras** | Cualquier cosa que no entre en las categorías anteriores. |

El menú también muestra **conectores** (por ejemplo, _Examinar Marketo_ abre un cuadro de diálogo de selección) y **accesos directos de navegación** que lo llevan a una pantalla de área de trabajo.

### Seleccionar un elemento de menú

Cuando selecciona una aptitud o un agente en el menú, se inserta un mensaje de inicio en el cuadro de mensaje para que lo edite; se **no** envía automáticamente. Por ejemplo, si selecciona _Planificar campañas_ se descarta en _&quot;Planificar un nuevo programa de Marketo para [nombre de campaña]. Voy a cargar el informe.&quot;_ Rellene los marcadores de posición entre corchetes y presione **Intro** para enviar.

Los conectores abren un modal en lugar de insertar texto. Los métodos abreviados de navegación le llevan directamente a esa pantalla del espacio de trabajo.

>[!NOTE]
>
>Algunos comandos aparecen atenuados y marcados _Próximamente_. Estas están cerradas por indicadores de funcionalidades y aún no están activas para su cuenta: seleccionar una no hace nada. El conjunto disponible depende de las funciones que estén habilitadas para usted.

## Habilidades

Una aptitud es un flujo de trabajo empaquetado que el agente sabe cómo ejecutar: los componentes básicos del menú `/` y de las solicitudes en lenguaje natural. Cada aptitud agrupa instrucciones paso a paso y las herramientas específicas necesarias para un trabajo (por ejemplo, &quot;publicar un recorrido&quot;, &quot;comparar dos listas de personas&quot;, &quot;crear un modelo de puntuación&quot;).

Consulte _[Habilidades de compañero](./skills.md)_ para obtener una lista completa de las habilidades que admite actualmente.

Aspectos clave que hay que saber sobre las aptitudes:

* **Las aptitudes tienen alcance de producto.** En [!DNL Marketo Optimizer] verá varias habilidades específicas del producto (recorridos, listas de personas, puntuación, canales, optimización del tiempo de envío, etc.). Algunas habilidades son solo [!DNL Marketo Engage] y un par de ellas trabajan en ambos productos (importación de posibles clientes, conocimiento del producto). Solo ve aptitudes relevantes para el lugar en el que se encuentra.
* **No es necesario que memorice los nombres de aptitudes.** Describa su objetivo y el agente elegirá la aptitud coincidente. El menú `/` es un método abreviado más rápido y reconocible para los mismos flujos de trabajo.
* **Algunas habilidades solo se leen; otras cambian las cosas.** Las aptitudes de investigación e informe (por ejemplo, investigación de posibles clientes, consulta por intención, informe de tiempo de envío) solo leen datos. Cree y configure aptitudes (por ejemplo, creación de recorridos, puntuación) para crear o cambiar datos.

## Mensajes de seguimiento

Después de las respuestas de los compañeros, a menudo se muestra una fila de mensajes de seguimiento en los que se puede hacer clic y adaptados a lo que acaba de hacer; por ejemplo, después de crear un recorrido, podría ofrecer _&quot;Publicar este recorrido&quot;_ o _&quot;Agregar un paso de espera&quot;_. Haga clic en uno para continuar sin escribir. Solo son sugerencias; siempre puede escribir su propio mensaje siguiente en su lugar.

## Sugerencias

* **Sea específico con los identificadores.** Al investigar o editar, incluya la dirección de correo electrónico, el nombre de la persona, el nombre del recorrido o el nombre de la lista para que el agente actúe en el recurso correcto.
* **Use `/` para explorar.** Si no está seguro de lo que puede hacer un compañero, abra el menú `/` y revise las categorías.
* **Edite la solicitud de inicio.** Si selecciona una aptitud, recibirá una plantilla; reemplace los `[bracketed]` marcadores de posición antes de enviar.
* **Cargue primero para importaciones.** Para una importación de posibles clientes, adjunte primero el archivo CSV y, a continuación, describa lo que desea hacer con él.
* **Inicia una nueva conversación** cuando cambies a una tarea no relacionada, por lo que el contexto anterior no afecta a la nueva solicitud.
