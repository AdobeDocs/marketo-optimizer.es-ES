---
title: Crear audiencias para programas
description: Utilice la habilidad Creación de audiencias en Marketo Optimizer para crear listas de personas, adaptar las listas inteligentes de Marketo Engage y editar las reglas de las listas en el chat.
source-git-commit: c00dc1d3f3028ece56905f9f1018605147b0ac20
workflow-type: tm+mt
source-wordcount: '1464'
ht-degree: 0%

---

# Creación de audiencias para programas

En [!DNL Adobe Marketo Optimizer], [_listas de personas_](../audiences/people-lists.md) definen la audiencia para los recorridos de personas, ya sea como listas dinámicas basadas en filtros que se actualizan automáticamente o como listas estáticas con pertenencia fija. Desde la [interfaz de chat](./chat-interface.md), la _creación de audiencias_ [habilidad](./skills.md) crea, adapta y edita listas de personas a través de una conversación guiada.

* **Habilidades** - `audience-creation` y `people-list-comparison`
* **Invocación**: describe los criterios de audiencia directamente, carga una lista inteligente [!DNL Marketo Engage] o nombra una lista existente para editar
* **Lee/escribe en** - [!DNL Marketo Optimizer]; lee [!DNL Marketo Engage] al adaptar listas inteligentes

## Flujos de trabajo admitidos {#workflows}

El compañero admite tres flujos de trabajo de creación de audiencias y determina cuál se aplica desde la solicitud. Si su intención es ambigua, pregunta antes de continuar.

| Flujo de trabajo | Cuándo se debe utilizar | Mensaje de ejemplo |
|---|---|---|
| **Crear desde cero** | Desea una nueva lista de personas definida por criterios o pertenencia. | _&quot;Crear una lista dinámica de los VP de marketing en las empresas SaaS de Norteamérica&quot;._ |
| **Adaptar una lista inteligente [!DNL Marketo Engage]** | Ya tiene una lista inteligente [!DNL Marketo Engage] o una campaña inteligente y quiere una lista de personas equivalente. | _&quot;Adaptar esta lista inteligente de Marketo a una lista de personas.&quot;_ (adjuntar el recurso) |
| **Editar una lista existente** | Desea agregar o reemplazar las reglas de una lista que ya tiene. | _&quot;Agregar una regla a mi lista de &#39;Ensayos empresariales&#39; para obtener una puntuación de posibles clientes superior a 50.&quot;_ |

## Crear una lista de personas desde cero {#create-from-scratch}

Antes de generar nada, el compañero de trabajo confirma las cuatro opciones siguientes. Solicita los que faltan, en un solo mensaje.

1. **Reglas / criterios**: una descripción en lenguaje sencillo de quién pertenece a la lista.
1. **Nombre** — Cómo llamar a la lista.
1. **Ubicación**: en qué programa debe residir la lista. Proporcione un nombre de programa y el Compañero de trabajo lo encontrará; si hay varias coincidencias, le pedirá que elija.
1. **Tipo**: dinámico (basado en filtros, actualización automática) o estático (pertenencia fija). Esto es obligatorio: el compañero no adivina; si no especifica, pregunta.

### Listas dinámicas {#dynamic-lists}

Para las listas dinámicas, el colaborador sugiere de forma proactiva incluir atributos de personalización para enriquecer la segmentación. Estos atributos están **_incluidos de forma predeterminada; usted decide excluirse, no en_**:

| Atributo | Por qué ayuda |
|---|---|
| **Persona derivada** | Comprador deducido por IA para la segmentación de contenido basada en persona. |
| **Intención derivada** | Señales de intención de compra deducidas que aparecen en las cuentas del mercado. |
| **Nivel de participación** | Nivel de participación calculado que prioriza los contactos comprometidos. |

Informe a su compañero si desea eliminar alguno de estos elementos antes de continuar.

### Listas estáticas {#static-lists}

* **Estática, sin criterios**: la lista se crea vacía, lista para que pueda agregar miembros manualmente.
* **Estático a partir de los criterios (una instantánea)**: el compañero crea el conjunto coincidente y copia a esas personas en. La población es asíncrona: el compañero confirma que la lista se ha creado, pero observa que las personas pueden tardar unos minutos en aparecer. No alegará que la lista está lista inmediatamente.

## Revisar tarjeta {#review-card}

No se crea nada hasta que lo apruebe. Después de describir los criterios, el compañero presenta una tarjeta _Revisión de creación de lista de personas_ interactiva (para las adaptaciones de las listas [!DNL Marketo Engage], la tarjeta se titula _Revisión de conversión de lista de personas_).

Cada fila de la tarjeta representa una condición:

| Columna | Significado |
|---|---|
| **Requisitos** (o el nombre de lista [!DNL Marketo Engage] para adaptaciones) | Su solicitud original o el filtro de Marketo de origen. |
| **(regla)** | La regla basada en atributos real generada para esa condición. |
| **Incluir** | Casilla de verificación para mantener o eliminar esa regla. |

**Niveles de confianza:**

* **Las filas de alta confianza** coinciden perfectamente y se comprueban de forma predeterminada.
* Las filas **Baja confianza** (asignaciones aproximadas o cualquier elemento marcado) se muestran con un indicador de aviso y están desactivadas de forma predeterminada.
* Las filas que el sistema no pudo asignar muestran **&quot;No se encontró ningún equivalente&quot;**; no tienen regla y permanecen desmarcadas.

Un _resumen de conversión_ cuenta _N alta confianza_ y _N baja confianza_, con una sugerencia: las reglas de baja confianza están desactivadas de forma predeterminada; márquelas para incluir o describir el cambio que desee en el chat.

**Acciones de tarjeta:**

* **Continuar**: crea la lista utilizando únicamente las reglas seleccionadas.
* **Describa los cambios que desee en el chat**: rellena previamente la entrada con _&quot;Deseo cambiar: &quot;_ para que pueda perfeccionarlo; el compañero se regenera y muestra una tarjeta nueva, conservando las reglas que ya había aprobado.

También puede escribir un seguimiento en cualquier momento (por ejemplo, _&quot;también restringido a compañías de más de 500 empleados&quot;_) y el Compañero de trabajo vuelve a generar la tarjeta.

## Asignación de atributos {#attribute-mapping}

Al describir los criterios, el colaborador traduce cada condición en un atributo real conocido de nivel de persona. En la tarjeta Revisar pueden aparecer tres resultados:

1. **Coincidente (alta confianza)**: su condición se asigna directamente a un atributo (por ejemplo, _&quot;el correo electrónico es acme.com&quot;_ se asigna al atributo `email`). Activada de forma predeterminada.
1. **Aproximado (poco fiable)**: el atributo disponible más cercano difiere en el nombre o el modelo de datos (por ejemplo, un filtro de Marketo _Cantidad_ aproximado como _Puntuación de posibles clientes_). Se muestra con una nota que explica la diferencia; desactivada de forma predeterminada.
1. **No encontrado** — La condición no se pudo asignar a ningún atributo conocido. Se muestra como _&quot;No se encontró ningún equivalente&quot;_; no se genera ninguna regla.

Por este motivo, es posible que una lista que describa vuelva con menos reglas que las condiciones especificadas: las condiciones no coincidentes aparecen explícitamente en lugar de perderse de forma silenciosa. Si los criterios importantes se clasifican como &quot;no encontrado&quot;, vuelva a expresarlos con el nombre real del atributo y los reintentos de Coworker.

>[!NOTE]
>
>Si va a asignar columnas de hoja de cálculo a campos (una tarjeta de asignación de campos con _Columna Source_, _Campo de destino_, un porcentaje de confianza y una lista de _Columnas no asignadas_), ese es el flujo de importación de posibles clientes, no la creación de audiencias. Ver la [aptitud para importar posibles clientes](./skills.md#audiences-people).

## Editar reglas para una lista existente {#edit-rules}

Cuando solicita cambiar las reglas de una lista que ya tiene, Coworker establece qué lista y qué modo de edición:

* **Agregar / anexar** (predeterminado para _&quot;agregar reglas&quot;_, _&quot;agregar más reglas&quot;_): las nuevas reglas se combinan con las existentes.
* **Reemplazar** (predeterminado para _&quot;reemplazar reglas&quot;_, _&quot;cambiar reglas a&quot;_): las nuevas reglas reemplazan todas las reglas existentes en la lista.

El compañero resume lo que se aplicará y establece claramente si se añade o reemplaza. A continuación, le pide que confirme antes de comprometerse. Después de la aplicación, informa del recuento total de reglas y de cuántas se añadieron o reemplazaron.

>[!NOTE]
>
>Las ediciones utilizan una ruta según la combinación, por lo que una operación &quot;añadir&quot; nunca sobrescribe de forma silenciosa las reglas existentes.

## Solapamiento de público {#overlap}

Pida a su compañero que compare listas de dos personas (por ejemplo, _&quot;Muéstreme la superposición entre &#39;Seminario web del tercer trimestre&#39; y &#39;Cuentas de empresa&#39;&quot;_) y procesará una tarjeta _Superposición de lista de personas_:

* Distintivo de encabezado que muestra el recuento: **&quot;{N} en común.&quot;**
* Una fila de estadísticas con el recuento total de miembros de cada lista y la superposición como **&quot;X% de A · Y% de B.&quot;**
* Una tabla de miembros de las personas de ambas listas, con una columna **Nombre** y una segunda columna que puede dirigir: **Correo electrónico** (predeterminado), **Compañía** o **Puesto**, según lo que haya preguntado.
* Haga clic en cualquier nombre para abrir esa persona en el espacio de trabajo.
* Si no hay superposición, la tarjeta indica claramente: _&quot;No hay miembros en común entre estas dos listas.&quot;_

**Limitaciones:**

| Límite | Detalles |
|---|---|
| **Tamaño de tabla** | Muestra hasta 200 miembros; más allá de eso, anota _&quot;Mostrando 200 de N — pídeme que refine la consulta para reducir los resultados.&quot;_ |
| **Cálculo de superposición** | Se calcula según la dirección de correo electrónico; las personas sin correo electrónico se excluyen de la intersección. |
| **Tamaño de lista** | Lee hasta aproximadamente los primeros ~1,000 miembros de cada lista. Para listas más grandes, Coworker le dice que los resultados son parciales. |
| **Listas dinámicas de borrador** | No se puede comparar: una lista que no se ha publicado no tiene ningún segmento activo. Su compañero le pedirá que lo publique primero o que utilice una lista estática en su lugar. |

## Validación de QA {#qa-validation}

Después de crear o actualizar una lista, el compañero ofrece: _&quot;¿Desea que compruebe que la lista está configurada correctamente?&quot;_ Si acepta, recupera la lista e informa de las siguientes comprobaciones:

| Marque | Resultado |
|---|---|
| La lista se encuentra en el programa o la carpeta correctos | Aprobado/suspenso |
| El recuento de filtros coincide con lo que se aplicó | _N_ filtros / no coinciden |
| Atributos de Personalization presentes (si se incluyen) | Presente/ausente |
| El nombre de la lista coincide con lo solicitado | Aprobado/suspenso |
| Recuento estimado de miembros | _count_ o N/A |

## Limitaciones {#limitations}

| Limitación | Detalles |
|---|---|
| **Adaptación de lista estática de[!DNL Marketo Engage]** | No puede adaptar una lista estática [!DNL Marketo Engage] (o un correo electrónico u otro recurso sin filtro) a una lista de personas. Las listas estáticas son ID de miembro explícitos y no se pueden expresar como filtros; en su lugar, Coworker solicita una lista inteligente o una campaña inteligente. |
| **Filtros basados en la actividad y la pertenencia** | Al adaptarse de [!DNL Marketo Engage], los filtros como _Se abrió el correo electrónico_, _Se completó la página web visitada_, _Se rellenó el formulario_, _Miembro de la lista_ y _Miembro de la campaña inteligente_ no tienen equivalente de lista de personas y regresan como &quot;No se encontró un equivalente&quot;. |
| **Condiciones a nivel de compañía** | Se traduce al atributo de nivel de persona más cercano siempre que sea posible (las listas de personas funcionan con atributos de persona) y se marca como de baja confianza cuando el ajuste es holgado. |
| **Lógica AND/OR profundamente anidada** | La lógica anidada compleja puede contraerse a un AND/OR de nivel superior; Coworker observa esto cuando sucede. |
| **Conflictos de nombres** | No se resuelve automáticamente: si se usa el nombre, Coworker le pedirá uno diferente en lugar de anexar silenciosamente un sufijo. |
| **Se requiere aprobación** | El compañero no creará ni modificará una lista hasta que haga clic en **[!UICONTROL Continuar]**, confirme o dé un visto bueno claro (_&quot;aprobado&quot;_, _&quot;se ve bien&quot;_, _&quot;compilarlo&quot;_). |
| **Población de instantáneas estáticas** | La pertenencia a listas estáticas creadas a partir de criterios se completa en unos minutos, no de forma inmediata. |

