---
title: Personas derivadas
description: Utilice personalidades derivadas en Marketo Optimizer para segmentar listas de personas y rutas de recorrido. Conozca las asignaciones de personas predeterminadas y el filtro Persona derivada.
TQID: 'https://experienceleague.adobe.com/5HAnnC6dbU-sE9dzBWs479z1H4LlNSkhhoNSrQxSfqI'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2:
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
  - id: a29661b8-f7a4-53d1-a9ac-fdec08c092e4
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 625
ht-degree: 0%

---

# Personas derivadas

La clasificación personal transforma los datos sin procesar de los clientes en una comprensión semántica del comprador que la IA puede utilizar para generar contexto y dirigir decisiones personalizadas en todos los canales y recorridos. Este perfil unificado proporciona lo siguiente:

* _ramificación de Recorridos_: las rutas divididas dirigen a los posibles clientes por persona, profundidad de participación y rol
* _Arbitraje de Recorrido_: determina a qué recorrido nutritivo pertenece un posible cliente en este momento, evitando conflictos de mensajes entre programas simultáneos
* _Personalización de contenido_: contenido que es narrativas específicas de funciones (&quot;para un ejecutivo&quot; o &quot;para un profesional&quot;)
* _Contexto de Sales Qualifier_: los representantes de desarrollo empresarial (BDR) reciben un resumen de una pantalla que muestra la identidad de la persona, sus intereses y su fase actual en el recorrido del comprador

## Personalidades predeterminadas {#default-ersonas}

En la versión de Beta de Marketo Optimizer, las siguientes personas predeterminadas se definen según el atributo del puesto:

| Persona | Títulos de trabajo |
| ------- | ---------- |
| [!UICONTROL CXO / EVP] | CEO, CIO, CTO, CMO, CFO, Vicepresidente Ejecutivo de Estrategia |
| [!UICONTROL SVP / VP] | vicepresidente senior de marketing, vicepresidente de ventas, vicepresidente de operaciones, vicepresidente de producto, vicepresidente de TI |
| [!UICONTROL Responsable principal / Responsable] | Director de Marketing, Director de TI, Director de Operaciones, Director de Ventas, Director de Recursos Humanos |
| [!UICONTROL Colaborador individual] | Ejecutivo de cuentas, Ingeniero de software, Especialista en marketing, Representante de éxito del cliente |
| [!UICONTROL Analista] | Analista de negocios, Analista de datos, Analista de investigación de mercado, Analista financiero, Analista de operaciones |
| [!UICONTROL Desarrollador] | Desarrollador front-end, desarrollador back-end, desarrollador de pila completa, desarrollador de aplicaciones móviles, ingeniero de DevOps |
| [!UICONTROL Personal del Cuadro Orgánico] | Especialista en Recursos Humanos, Asesor Jurídico, Oficial de Cumplimiento, Gerente de Proyectos, Especialista en Adquisiciones |
| [!UICONTROL Consultor] | Consultor de administración, consultor de TI, consultor de procesos empresariales, consultor de marketing |
| [!UICONTROL Otras] | Especialista en el sector, Asesor independiente, Consultor independiente, Experto en la materia |

>[!NOTE]
>
>En la próxima versión de General Availability, puede editar cualquiera de estas personalidades predeterminadas según las necesidades de su organización. También admite la asignación y las definiciones de personas personalizadas.

## Filtrar por persona derivada {#derived-persona-filter}

[!DNL Marketo Optimizer] deriva un perfil para cada registro de persona mediante la evaluación de los atributos de registro frente a los perfiles definidos. Puede utilizar el resultado deducido (_Persona derivada_) como filtro al definir la audiencia para una lista de personas o para segmentar en un recorrido de personas.

El filtro _[!UICONTROL Persona derivada]_ aparece en el panel de filtro bajo la categoría **[!UICONTROL Atributos de persona]**.

### Listas de personas {#people-lists}

Al administrar miembros en una [lista de personas estáticas](./people-lists.md#static-lists) o definir reglas para una [lista de personas dinámicas](./people-lists.md#dynamic-lists), puede filtrar por _Persona derivada_ para dirigirse a todas las personas cuyos atributos coincidan con una persona configurada específica.

![Filtro de persona derivado para una lista de personas](./assets/derived-persona-filter-people-list.png){width="750" zoomable="yes"}

**Lista estática — Agregar miembros**

1. Abra la lista estática y haga clic en **[!UICONTROL Agregar personas]** en la parte superior derecha.

1. En el cuadro de diálogo de filtro, expanda **[!UICONTROL Atributos de personas]** y arrastre **[!UICONTROL Persona derivada]** al lienzo.

1. En la condición de filtro, elija **[!UICONTROL is]** y seleccione una o más personalidades de la lista.

1. Haga clic en **[!UICONTROL Listo]** para aplicar el filtro y calificar a las personas coincidentes en la lista.

**Lista dinámica — Establecer reglas de pertenencia**

1. Abra la lista dinámica y seleccione la ficha **[!UICONTROL Reglas]**.

1. Haga clic en **[!UICONTROL Editar reglas]**.

1. En el cuadro de diálogo de filtro, expanda **[!UICONTROL Atributos de personas]** y arrastre **[!UICONTROL Persona derivada]** al lienzo.

1. En la condición de filtro, elija **[!UICONTROL is]** y seleccione una o más personalidades de la lista.

1. Haga clic en **[!UICONTROL Listo]** para guardar la regla.

   La pertenencia se actualiza automáticamente a medida que se evalúan los registros de persona según la regla.

### Recorridos de persona {#person-journeys}

Al configurar la segmentación para un recorrido de persona en un nodo [_Split paths_](../marketing/split-merge-paths-nodes.md), puede usar un perfil derivado como un filtro de perfil de persona para controlar qué personas ingresan a la ruta de recorrido.

![Filtro de persona derivada para una condición de ruta dividida](./assets/derived-persona-filter-split-path.png){width="750" zoomable="yes"}

1. Haga clic en el nodo **[!UICONTROL Dividir rutas]** en el lienzo de recorrido.

1. En el panel de propiedades del nodo de la derecha, haga clic en **[!UICONTROL Aplicar condición]** o **[!UICONTROL Editar condición]** para una ruta.

1. En el cuadro de diálogo de filtro, expanda **[!UICONTROL Atributos de personas]** y arrastre **[!UICONTROL Persona derivada]** al lienzo.

1. En la condición de filtro, elija **[!UICONTROL is]** y seleccione una o más personalidades de la lista.

1. Haga clic en **[!UICONTROL Listo]** para guardar el filtro de la ruta.

