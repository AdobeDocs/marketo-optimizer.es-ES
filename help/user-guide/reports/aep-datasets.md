---
title: Conjuntos de datos Experience Platform
description: Obtenga información sobre los conjuntos de datos que Marketo Optimizer escribe en Adobe Experience Platform para impulsar la creación de informes y las consultas ad hoc de Customer Journey Analytics.
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
source-git-commit: 1ebb0036699252c50f33ba6c0f4a56e8e670aacd
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 4%
---

# Conjuntos de datos Experience Platform

[!DNL Adobe Marketo Optimizer] replica datos de clientes potenciales, recorridos y actividades en [!DNL Adobe Experience Platform] conjuntos de datos. Estos conjuntos de datos alimentan la página [!UICONTROL Informes] y la experiencia de informe [!DNL Adobe Customer Journey Analytics] incrustada. También puede consultarlos directamente con [!DNL Query Service] para Ad Hoc Analysis.

Los conjuntos de datos están administrados por el sistema. Una conexión en [!DNL Customer Journey Analytics] los vincula a la vista de datos que utilizan los informes de [!DNL Marketo Optimizer], por lo que no es necesario que genere esta conexión usted mismo. Esta conexión es la misma conexión a la que se llega cuando se selecciona **[!UICONTROL Analizar en CJA]** en una sección de informe. Ver [Analizar un informe en Customer Journey Analytics](./reports-overview.md#analyze-a-report-in-cja).

## Conjuntos de datos disponibles {#available-datasets}

Los siguientes conjuntos de datos se rellenan para cada instancia de [!DNL Marketo Optimizer].

>[!NOTE]
>
>Cada nombre de conjunto de datos utiliza el prefijo `AJOB2B`, que indica el nombre del sistema para los datos [!DNL Marketo Optimizer]. Se espera este comportamiento y puede usar estos nombres para localizar los conjuntos de datos en su zona protegida [!DNL Experience Platform].

| Conjunto de datos | Esquema | Descripción |
| --- | --- | --- |
| `AJOB2B - Person` | Persona | Atributos de posible cliente estándar. |
| `AJOB2B - PersonActivity` | Actividad de persona | Eventos de actividad asociados a una persona. |
| `AJOB2B - PersonActivityType` | Tipo de actividad de persona | Tipos de actividades asociadas a una persona. |
| `AJOB2B - PersonActivityTypeEngagementMapping` | Asignación de participación de tipo de actividad de persona | Asigna los tipos de actividades a su clasificación de participación, evento de canal y direccionalidad. |
| `AJOB2B - Journey` | Recorrido | Lista de recorridos y sus metadatos de ciclo vital. |
| `AJOB2B - JourneyNode` | Nodo de recorrido | Lista de nodos dentro de un recorrido y sus metadatos asociados. |
| `AJOB2B - EngagementAsset` | Recurso de participación | Búsqueda unificada de ID de recursos de participación y nombres para mostrar en todos los tipos de recursos de participación. |

## Consultar conjuntos de datos con el servicio de consultas {#query-service}

Use [!DNL Query Service] para ejecutar consultas SQL ad hoc en estos conjuntos de datos cuando necesite análisis fuera de [!DNL Customer Journey Analytics] informes. El acceso a consultas requiere los permisos adecuados de [!DNL Experience Platform] para la zona protegida. Para obtener información general sobre la sintaxis y configuración de consultas, consulte [Servicio de consultas](https://experienceleague.adobe.com/es/docs/experience-platform/query/home){target="_blank"}.

![Editor del servicio de consultas que muestra una consulta SELECT en el conjunto de datos de ajob2b_recorrido y una tabla de registros de recorrido resultantes.](./assets/aep-query-service.png){width="800" zoomable="yes"}

>[!NOTE]
>
>Estos conjuntos de datos son de solo lectura. Para cambiar los datos que captura [!DNL Marketo Optimizer], actualice los datos de origen en [!DNL Marketo Optimizer] o [!DNL Marketo Engage] en lugar de editar un conjunto de datos directamente.
