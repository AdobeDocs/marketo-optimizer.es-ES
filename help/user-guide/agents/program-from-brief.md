---
title: Creación de un programa a partir de un resumen
description: Utilice la aptitud Creación de programas en Marketo Optimizer para crear programas, tokens, listas de personas y recorridos a partir de un informe de campaña.
TQID: 'https://experienceleague.adobe.com/Bi7ZemHiGpKwxsYZkrfCyT5IzFAJ8ZTyFr8KxwO4z6w'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 1650dadf-b034-5ac9-a309-77ad1e2f5035id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1id: a29661b8-f7a4-53d1-a9ac-fdec08c092e4
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 1110
ht-degree: 4%

---

# Creación de un programa a partir de una descripción breve

En [!DNL Adobe Marketo Optimizer], [_program_](../marketing/programs.md) es el contenedor de nivel superior para recorridos, listas de personas, tokens y configuración dentro de una campaña. Desde la [interfaz de chat](./chat-interface.md), la aptitud para la creación de programas desarrolla toda esa estructura de un extremo a otro a partir de las instrucciones (el programa en sí, las subcarpetas, los tokens, las listas de personas y los recorridos de personas) en una sola conversación guiada.

* **Habilidad** - `program-creation`
* **Invocación** - Cargue un informe e ingrese _Cree un programa a partir de este informe_ / _Genere un programa a partir del informe_, o describa la campaña directamente
* **Lee/escribe en** - [!DNL Marketo Optimizer]; también lee la configuración de tipo de programa de su inquilino

## Carga breve

Haz clic en el icono _Adjuntar_ en la entrada del chat para cargar el archivo y, a continuación, describe lo que deseas. El texto de la información se extrae y se entrega al compañero como contexto (verá un indicador &quot;Resumen de campaña cargado: nombre de archivo (NkB)&quot; en el chat).

### Tipos de archivos compatibles

| Formato | Comportamiento |
|---|---|
| `.txt`, `.md` | Leer directamente en el explorador |
| `.pdf`, `.docx`, `.xlsx`, `.json`, `.csv` | Enviado al servicio de extracción de texto del servidor |

Un archivo con un nombre que contiene *brief* se etiqueta automáticamente como un resumen de campaña; de lo contrario, Coworker lo deduce del contexto.

### Límite de tamaño

El texto breve se trunca a aproximadamente 30 000 caracteres (~7500 tokens) antes de llegar a Coworker. Los informes muy largos se cortan en ese punto (indicado por una nota de `(truncated to 29KB)`). Coloque los detalles esenciales de la campaña por adelantado.

## Contenido breve recomendado

La entrada de flujo lee el resumen de las siguientes entradas (incluir tantas como sea posible):

* Nombre del programa y una breve descripción/propósito
* Señal de tipo de programa (como feria comercial, evento, seminario web, gira, conferencia o formación)
* Criterios de audiencia para las listas de personas
* Diseño del recorrido: recuento, criterios de entrada, puntos de contacto/tiempo y una fecha de lanzamiento
* Tokens (valores reutilizables como fecha del evento, lugar de celebración, línea de asunto)

El compañero solicita cualquier cosa que falte antes de crear.

## Fases de compilación

La aptitud se ejecuta en tres fases: **ADMISIÓN → APROBACIÓN → COMPILACIÓN**. No se crea nada hasta que se aprueba.

### Admisión

El compañero extrae lo siguiente de las instrucciones y le pide que especifique si le falta algo:

* Nombre del programa
* Carpeta principal (de forma predeterminada raíz del espacio de trabajo si no se especifica)
* Descripción
* Tipo de programa (deducido de una redacción breve siempre que sea posible)
* Tokens para crear (nombre, tipo, valor)
* Criterios de audiencia de lista de personas
* Recorridos: recuento, criterios de entrada, puntos de contacto, fecha de lanzamiento

### Aprobar

El compañero presenta un resumen de confirmación antes de continuar:

`I'll create {program} in folder {id}, with {N} token(s), {N} dynamic people list(s), and {N} journey(s). Shall I proceed?`

No se llama a ninguna herramienta de creación hasta que respondas con una aprobación clara (como _continuar_, _continuar_, _compilarla_, _aprobada_ y _sí_).

### Generar

Los pasos de generación se ejecutan en un orden fijo; cada uno depende de los ID producidos por el paso anterior.

| Paso | Descripción | Herramientas | Output |
|---|---|---|---|
| **1. Carpeta** | Resuelve la carpeta principal por nombre o utiliza la raíz del espacio de trabajo; puede crear una nueva subcarpeta | `getRootTree`, `browseFolders`, `createFolder` | Nombre de carpeta + ID |
| **1.5. Tipo de programa** | Busca los tipos de programas de inquilino y elige la coincidencia para el informe | `browseProgramTypes` | Escriba el nombre + `programTypeId` |
| **2. Programa** | Crea el programa en la carpeta resuelta, enlazada al tipo elegido | `createProgram` | Nombre, ID y tipo del programa |
| **3. Tokens** | Crea cada token `my.*` en el programa | `createProgramToken` | Nombres de token |
| **4. Listas de personas** | Genera reglas basadas en atributos a partir de criterios de audiencia y crea la lista de personas dinámica | `generate_ruleset`, `createSmartListWithRules` | Nombre de lista + `smartListId` |
| **5. Recorridos** | Crea el recorrido de cada persona con un nodo de entrada de audiencia de persona conectado a la lista del paso 4 | `create_journey` | nombres de recorrido, ID |
| **6. Publicar** | Publica o programa el recorrido si se establece y confirma una fecha de lanzamiento | `publish_journey_with_dates` | Recorrido activo/programado |
| **7. QA** | Previsualización de validación opcional y comprobación de control de calidad completa | `qa_program_preview`, `qa_program` | Informe de aprobado/suspenso/advertencias |

**_Dependencias de paso:_**

* El ID de programa (paso 2) es necesario para que se puedan adjuntar tokens, listas o recorridos.
* El `smartListId` del paso 4 se pasa a `create_journey` en el paso 5, omitiendo que deje vacío el nodo de entrada de audiencia del recorrido.
* La solicitud de recorrido siempre comienza _Comience con un nodo de audiencia de persona como punto de entrada_ para garantizar que se rellene un nodo de entrada.

## Recursos de salida

### Programa

El contenedor de nivel superior. Su vista de detalles expone las siguientes pestañas:

| Tabulación | Contenido |
|---|---|
| **Información general** | Nombre, descripción, tipo de programa, estado, ubicación de carpeta, marcas de tiempo |
| **Atributos** | Campos personalizados definidos por el tipo (solo si el tipo de programa los habilita) |
| **Tokens** | `my.*` tokens con ámbito en este programa |
| **Recorridos** | Recorridos incluidos en el programa |

### Tokens

Valores `my.*` reutilizables con ámbito en el programa (p. ej. `my.eventDate`). Cada uno tiene un tipo (uno de `text`, `date`, `rich text`, `score` o `number`) y un valor. Se resuelven dentro de los correos electrónicos y el contenido dentro del ámbito del programa.

### Lista de personas

Una lista de personas dinámica (inteligente) creada a partir de criterios de audiencia mediante reglas generadas basadas en atributos y creadas bajo el programa.

### Recorrido

Un recorrido de persona que comienza con un nodo de entrada de audiencia de persona enlazado a la lista de personas del paso 4, seguido de los puntos de contacto de la información breve (por ejemplo, _enviar correo electrónico de bienvenida después de 1 día, seguimiento después de 3 días_). Si se establece una fecha de lanzamiento, el recorrido se puede publicar inmediatamente o programar.

## Resolución de tipo de programa

Los programas están **enlazados permanentemente** a un tipo de programa definido por el inquilino durante la creación; esto no se puede cambiar posteriormente. El flujo resuelve el tipo explícitamente mediante `browseProgramTypes` en cada caso.

| Caso | Comportamiento |
|---|---|
| **Hay varios tipos disponibles** | Hace coincidir una redacción breve con un tipo (como feria comercial/stand/expo = *feria comercial*/*evento*; seminario web = *seminario web*/*evento*; crianza/goteo = *crianza*; sin señal clara = *Predeterminado*). Si no se encuentra ninguna coincidencia, el colaborador enumera los tipos y tareas disponibles. |
| **Inquilino solo predeterminado** | Usa *Default* y observa que un administrador puede agregar [tipos de programa](../admin/program-types.md) personalizados. |
| **No hay tipos configurados** | Se detiene: la creación fallaría. Solicita a un administrador que aprovisione tipos de programas antes de volver a intentarlo. |

## Valores predeterminados

| Configuración | Predeterminado |
|---|---|
| **Carpeta** | Raíz de Workspace (si no se especifica ninguna carpeta) |
| **Tipo de programa** | *Predeterminado* (si no hay señal breve ni selección manual) |
| **Atributos de Personalization** | Persona derivada, Intención derivada, Nivel de participación incluido de forma predeterminada (opción de exclusión disponible) |
| **Publicación** | No es automático para futuras fechas de lanzamiento; se indica como un paso manual de `ACTIVATE journey by {date}`; la publicación inmediata solo se realiza al iniciar ahora y se confirma |
| **Puerta de aprobación** | No se crea ningún recurso antes de la aprobación explícita |

## Limitaciones

| Limitación | Detalles |
|---|---|
| **Límite de longitud breve** | ~30K caracteres; los maletines truncados pierden contenido final — ponga lo esencial primero |
| **Tipo de programa inmutable** | No se puede cambiar después de la creación. Compruebe el tipo correcto antes de aprobar |
| **Campos internos requeridos** | `parent` y `programTypeId` siempre están establecidos; omitir `parent` causa acceso denegado; omitir el tipo se recupera silenciosamente a *Predeterminado* |
| **El Recorrido requiere la lista de personas** | El `smartListId` del paso 4 es obligatorio para el paso 5; el flujo aplica esto |
| **Pertenencia a lista asíncrona** | Las listas estáticas (a partir de criterios) se rellenan en varios minutos, no de forma instantánea |
| **Tratamiento de errores** | Los errores de las herramientas se registran con el error exacto; el compañero solicita confirmar la entrada y volver a intentarlo |
| **Conflictos de nombres** | No resuelto automáticamente: se solicitará un nombre diferente |
| **Ámbito** | Solo Marketo Optimizer; los usuarios de [!DNL Marketo Engage] deben utilizar las habilidades de creación/planificación de programas por separado |


## Comprobación de control de calidad

Una vez finalizada la compilación, el colaborador ofrece lo siguiente:

> &quot;¿Desea que realice una comprobación de control de calidad para validar todo antes del lanzamiento?&quot;

Confirme que quiere ejecutar `qa_program_preview` seguido de `qa_program`. El proceso devuelve un informe de las comprobaciones realizadas, los errores y las advertencias, así como los pasos siguientes recomendados.
