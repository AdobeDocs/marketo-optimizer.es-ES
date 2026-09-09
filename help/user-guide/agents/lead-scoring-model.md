---
title: Crear modelos de puntuación personalizados
description: Cree, previsualice y publique modelos de puntuación de posibles clientes personalizados en Marketo Optimizer con la habilidad Scoring Studio en la interfaz de chat de Coworker.
TQID: 'https://experienceleague.adobe.com/OAY0CzFPTyUi7NCPbRnxGkG6nnndPygbwGlbv9u2oeA'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 1650dadf-b034-5ac9-a309-77ad1e2f5035
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 468
ht-degree: 1%

---

# Crear modelos de puntuación personalizados

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_scoring_studio"
>title="Puntuación de Studio"
>abstract="Utilice la habilidad Scoring Studio para crear, configurar y publicar modelos de puntuación de posibles clientes personalizados a través de la interfaz de chat de Coworker."

La aptitud [_Scoring Studio_](./skills.md#scoring-signals) en [!DNL Adobe Marketo Optimizer] proporciona una solución de puntuación de posibles clientes nativa de IA que le permite crear, configurar y publicar modelos de puntuación de posibles clientes. El estudio combina un flujo de trabajo impulsado por el agente con una interfaz de usuario visual: puede crear modelos de puntuación mediante mensajes en lenguaje natural en la [interfaz de chat de Coworker](./chat-interface.md) o interactuando directamente con los controles de la interfaz de usuario.

* **Habilidad** - `scoring-studio`
* **Invocación**: use un comando de barra para abrir Scoring Studio. Por ejemplo: _&quot;abrir Scoring Studio.&quot;_
* **Lee/escribe en** - servicio de puntuación [!DNL Marketo Optimizer]; lee [!DNL Marketo Engage] campos de posibles clientes y tipos de actividades

En el inicio, el colaborador recupera automáticamente el contexto relevante, incluidos los tipos de actividad, los campos de posibles clientes, las listas de personas y las listas de puntuación existentes, para fundamentar sus sugerencias en los datos.

![Se inició Scoring Studio en la interfaz de chat de Coworker](./assets/scoring-studio.png){width="700" zoomable="yes"}

## Crear un modelo de puntuación {#create-model}

Al abrir Scoring Studio, el colaborador propone un modelo de puntuación de ejemplo relevante previamente rellenado con una lista estática y un conjunto de actividades puntuadas. Puede aceptar este punto de partida sugerido o proporcionar su propio indicador para definir un modelo personalizado.

### Previsualización del modelo {#preview-model}

Después de enviar un mensaje, el colaborador genera una vista previa del modelo antes de realizar cualquier cambio. Las superficies de previsualización:

* Dimensiones de puntuación en uso
* Atributos y actividades que se clasifican
* Listas estáticas o listas inteligentes aplicadas como segmentos
* Resumen de la meta del modelo, el segmento de destinatario y las señales principales

Puede revisar la vista previa y elegir crear el modelo basado en él, o continuar refinando a través del chat antes de finalizar.

### Estructura del modelo {#model-structure}

El modelo creado está organizado en _dimensiones_ y _señales_. Puede configurar cada señal mediante el panel de propiedad en la interfaz de usuario de:

* **Tipo de señal** — Basada en actividades o en atributos
* **Actividad o atributo**: El elemento específico que se va a puntuar
* **Parámetros de señal** — Ajustes ajustables para la señal

Puede crear y configurar modelos completamente mediante Coworker con lenguaje natural o interactuar directamente con los controles de la interfaz de usuario.

## Publicar un modelo de puntuación {#publish-model}

Cuando finalice el modelo, indique a su compañero que lo publique. El proceso de publicación gestiona automáticamente lo siguiente:

| Paso | ¿Qué sucede? |
|---|---|
| **Compilación de reglas** | Todas las reglas de puntuación se compilan y validan |
| **Creación de tarea de puntuación** | Se crea una tarea de puntuación programada y se configura para ejecutarse diariamente |

Después de la publicación, también tiene la opción de almacenar en déclencheur una ejecución manual para procesar las puntuaciones inmediatamente.

## Ver resultados de puntuación {#view-results}

Cuando finaliza una ejecución de puntuación, las puntuaciones se vuelven a escribir en [!DNL Marketo Engage] mediante el proceso de importación de posibles clientes. Una vez completada la importación, las puntuaciones actualizadas se pueden comprobar directamente en [!DNL Marketo Engage].

Después de cada ejecución, puede ver un resumen de los resultados que muestra lo siguiente:

* Cuántas personas se puntuaron
* La puntuación individual cambia por persona

Hay disponible un registro de auditoría para revisar los detalles adicionales de la ejecución.
