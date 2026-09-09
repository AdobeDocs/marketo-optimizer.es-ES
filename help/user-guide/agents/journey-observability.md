---
title: Progresión del Recorrido de monitorización y depuración
description: Aprenda a utilizar la habilidad Observabilidad del Recorrido en el chat de Coworker para depurar y supervisar cómo se mueven las personas y los posibles clientes a través de los recorridos, las decisiones de ruta dividida y el tiempo.
TQID: 'https://experienceleague.adobe.com/Pnd1fVWUZ-g27UDE-y6Pc2Qwjsx-1pDSCaTGxjrBTRc'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 1650dadf-b034-5ac9-a309-77ad1e2f5035id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 634
ht-degree: 0%

---

# Monitorización y depuración de la progresión del recorrido

La habilidad [_Observabilidad del Recorrido_](./skills.md#journeys) en [!DNL Adobe Marketo Optimizer] responde a preguntas sobre el lenguaje natural acerca de cómo las personas y los posibles clientes se mueven a través de los recorridos. Utilícelo en la [interfaz de chat de Coworker](./chat-interface.md) para seguir la progresión, comprender las decisiones de las rutas divididas, analizar a las personas dentro de los nodos de recorrido y comprobar las métricas de tiempo. También puede preguntar sobre los patrones de conducta entre recorridos.

* **Habilidad** - `journey-observability`
* **Invocación**: haz una pregunta en lenguaje natural o usa un comando de barra diagonal para ejecutar la habilidad de observación de Recorrido. Por ejemplo: _&quot;¿Cómo se movió demo_ lead_24@company.com a través de LeadNutureJourney?&quot;_
* **Lee de** - [!DNL Marketo Optimizer] datos de recorrido; lee [!DNL Marketo Engage] listas estáticas para comprobar la pertenencia a la lista

## Ver detalles de la persona o el posible cliente {#person-details}

Solicite detalles básicos de solo lectura sobre una persona o le lleve a establecer un contexto antes de investigar su recorrido. Proporcione la dirección de correo electrónico, el ID de posible cliente o el nombre del posible cliente de la persona.

* _&quot;Proporcionarme información básica sobre el posible cliente demo_ lead_24@company.com.&quot;_
* _&quot;¿Cuál es el cargo y el país para el perfil john.doe@company.com?&quot;_
* _&quot;Mostrarme el correo electrónico y el rol de lead_ 01.&quot;_

## Seguimiento de la progresión mediante un recorrido {#journey-progression}

Pregunte cómo se movió una persona o posible cliente a través de un recorrido para ver la entrada, salida, duración y ruta a nivel de nodo que tomó. Proporcione la dirección de correo electrónico o el ID de posible cliente de la persona y el nombre del recorrido.

* _&quot;¿Cómo se movió demo_ lead_24@company.com a través de LeadNutureJourney?&quot;_
* _&quot;¿Qué nodos pasó john.doe@company.com en el recorrido de demostración del producto?&quot;_

## Comprensión de las decisiones de ruta dividida {#split-path-analysis}

Pregunte por qué una persona o posible cliente tomó, o no tomó, una ruta específica en un nodo dividido. Recorrido Observability explica la decisión utilizando los valores de atributo evaluados en ese momento. Proporcione la dirección de correo electrónico o el ID de posible cliente de la persona, el nombre del recorrido y el ID del nodo dividido.

* _&quot;¿Por qué demo_ lead_24@company.com fue a la ruta &#39;Altamente comprometida&#39; en el nodo dividido c764a9?&quot;_
* _&quot;¿Por qué john.doe@company.com no tomó la ruta calificada en el nodo ab123f en LeadNutureJourney?&quot;_
* _&quot;Compare por qué lead_ 01 y lead_02 tomaron rutas diferentes en el nodo dividido x99f3b.&quot;_

## Analizar personas en nodos de recorrido {#node-analysis}

Solicite recuentos de personas o posibles clientes y detalles dentro de un nodo de recorrido o ruta dividida. Filtre los resultados por persona, función, ubicación o nivel de participación. Proporcione el ID del nodo.

* _&quot;Asigne todas las personas que se encuentran actualmente en la ruta de &#39;participación alta&#39; del nodo node-459c7c.&quot;_
* _&quot;¿Cuántos posibles clientes hay en el nodo de calificación del recorrido de nutrición de demostración?&quot;_
* _&quot;Mostrarme posibles clientes en la ruta de acceso dividida &#39;Con intención baja&#39; filtrada por el rol: Administrador de marketing.&quot;_

## Identificación de patrones en recorridos {#pattern-recognition}

Pida a la Observabilidad del Recorrido que identifique rutas comunes, puntos de entrega y comportamientos repetidos a través de un recorrido. Proporcione el nombre del recorrido y, opcionalmente, un periodo de tiempo, persona, producto o cuenta para reducir los resultados.

* _&quot;¿Cuáles son las rutas más comunes que toman los SDR en el recorrido de demostración del producto?&quot;_
* _&quot;¿En qué punto de los posibles clientes suelen dejarse caer en el LeadNutureJourney?&quot;_
* _&quot;¿Hay retrasos inusuales o rutas inesperadas en el recorrido de nutrición Q1?&quot;_

## Comprobación de métricas operativas y de tiempo {#operational-metrics}

Pregunte por los tiempos de entrada, las duraciones de espera, la latencia de transición y la progresión estancada de un recorrido. Proporcione el nombre del recorrido y, opcionalmente, un ID de nodo o un identificador de persona.

* _&quot;¿Cuándo entró john.doe@company.com al recorrido de seguimiento de demostración?&quot;_
* _&quot;¿Cuánto tiempo suelen esperar los posibles clientes en el nodo de calificación en LeadNutureJourney?&quot;_
* _&quot;¿Qué posibles clientes llevan más de siete días paralizados en el recorrido de seguimiento de demostración?&quot;_

## Limitaciones {#limitations}

| Limitación | Detalles |
|---|---|
| Edición de atributos de persona o posible cliente | No compatible. Actualizar los registros de personas y posibles clientes directamente en [!DNL Marketo Engage] o [!DNL Marketo Optimizer]. |
| Crear, editar, pausar o reanudar recorridos | No compatible. En su lugar, usa el [lienzo de recorrido](../marketing/person-journeys.md) o una habilidad de edición de recorrido en [aptitudes de compañero](./skills.md#journeys). |
| Cambio de la lógica de división o la configuración de recorrido | No compatible. Editar rutas de acceso divididas directamente en el [lienzo de recorrido](../marketing/split-merge-paths-nodes.md). |
| Composición de grupos de compra o resúmenes a nivel de cuenta | Fuera de ámbito. Recorrido Informes de observabilidad solo a nivel de persona y posible cliente. |
| Cambio de horarios de recorrido o temporización | No compatible. |
