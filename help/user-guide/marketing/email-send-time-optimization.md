---
title: Optimización del tiempo de envío del correo electrónico
description: Configure la optimización del tiempo de envío en los recorridos de persona de Marketo Optimizer. Establezca ventanas de envío, agregue nodos de espera y vea informes de STO en Coworker.
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 0%

---

# Optimización del tiempo de envío del correo electrónico

Utilice la función de optimización del tiempo de envío (STO) para personalizar el tiempo de envío del correo electrónico para [recorridos de personas](./person-journeys.md) mediante la predicción de cuándo es más probable que se involucre cada perfil. En lugar de un tiempo de envío fijo, STO utiliza señales de participación de correo electrónico históricas para programar la entrega en el momento óptimo para cada destinatario, lo que mejora la participación general.

STO analiza la participación histórica de cada perfil mediante un modelo de lenguaje de gran tamaño. Predice y clasifica los tiempos de envío potenciales y luego programa el envío en la hora de mayor clasificación dentro de la ventana de optimización.

Las perspectivas de rendimiento, como el uso, el alza de la participación y las comparaciones de STO frente a no STO, están disponibles a través de consultas en lenguaje natural en Coworker.

>[!BEGINSHADEBOX]

Hay muchas **_mejoras futuras_** planificadas para STO:

* Configuración global de STO en el área _[!UICONTROL Admin]_
* Habilitación de STO de nivel de recorrido
* Divisiones de prueba/control configurables

>[!ENDSHADEBOX]

## Configuración {#configuration}

Puede configurar la optimización del tiempo de envío cuando [agregue un nodo _[!UICONTROL Realizar una acción]_](./action-nodes.md) al recorrido de una persona y elija la acción **[!UICONTROL Enviar correo electrónico]**.

1. Seleccione el nodo de acción de recorrido _Enviar correo electrónico_.

1. En las propiedades del nodo, a la derecha, habilite la opción **[!UICONTROL Optimización del tiempo de envío]**.

   ![Enviar nodo de recorrido de correo electrónico - Opciones de optimización del tiempo de envío](./assets/email-node-send-time-optimization.png){width="450" zoomable="no"}

1. Para especificar la ventana y la distribución de prueba, defina las opciones de STO:

   * **[!UICONTROL Enviar en el plazo del siguiente]**: este valor determina la ventana de optimización (en días), que es el intervalo de tiempo en el que se pueden enviar los correos electrónicos. Por ejemplo, para un seminario web que se produzca en cinco días, puede establecer una ventana de cuatro o cinco días. STO selecciona el tiempo de envío mejor predicho para cada perfil dentro de esta ventana.

   * **STO / Fixed distribution** - STO crea automáticamente una _división de prueba y control_ para dividir los perfiles elegibles entre los tiempos de envío optimizados y fijos. La división permite la comparación directa del rendimiento. (Las futuras mejoras están planificadas para permitir porcentajes de división personalizados).

   >[!NOTE]
   >
   >Los perfiles con un historial de participación sólido se dividen uniformemente en grupos de control y prueba para medir el impacto del STO. Para garantizar resultados estadísticamente fiables, la división de STO frente a no STO se restringe entre el 30 % y el 70 %. Esto ayuda a evitar que cohortes más pequeñas distorsionen los resultados y garantiza comparaciones significativas.

1. Justo después del nodo _[!UICONTROL Enviar correo electrónico]_, [agregue un nodo _Wait_](./wait-nodes.md).

   Un nodo de espera debe seguir inmediatamente a una acción de correo electrónico habilitada para STO. Añadir este nodo garantiza que los perfiles permanezcan en la recorrido hasta que se borre la ventana de optimización completa y se completen todos los envíos de STO. Si omite este nodo, el sistema marca la configuración como no válida.

1. Después de completar el resto del recorrido de la persona, continúe con [publicar](./person-journeys.md#publish).

## Sistema de informes {#reporting}

Los datos de rendimiento de STO están disponibles a través de [Coworker](../agents/chat-interface.md) con la aptitud `send-time-report`. Puede ver un informe de nivel de recorrido que resuma todos los nodos de correo electrónico, o explorar en profundidad un informe de nivel de nodo para una acción de correo electrónico específica.

El informe muestra cada nodo de correo electrónico del recorrido e indica si STO está habilitado para él. También muestra una comparación tabular entre los correos electrónicos con y sin STO para que pueda evaluar el alza de participación.

### Generación del informe STO {#generate-sto-report}

Existen tres formas de generar un informe de STO con el colaborador:

**Usar el comando de barra diagonal**

1. En el panel Compañero de trabajo, escriba `/` para mostrar la lista de aptitudes disponibles.
1. Seleccione **[!UICONTROL send-time-report]** de la lista y haga clic en la flecha hacia arriba para enviar la consulta.

   ![Consulta de aptitud de informe de tiempo de envío de compañero](./assets/email-sto-reporting-coworker.png){width="700" zoomable="yes"}

   Si un recorrido está abierto en el editor, Coworker lo utiliza como contexto automáticamente. De lo contrario, el Compañero de trabajo le pedirá que especifique el recorrido.

   El compañero carga el informe y muestra una tarjeta de resumen.

1. Haga clic en **[!UICONTROL Abrir informe]** para ver el informe completo con detalles de nivel de nodo.

**Haga clic en un nodo de correo electrónico**

1. En el lienzo del recorrido, haga clic en el nodo **[!UICONTROL Enviar correo electrónico]**.

1. En el panel Compañero de trabajo, solicite el informe STO.

   Como el nodo está seleccionado, el colaborador lo utiliza como contexto y devuelve un informe con ámbito solo para ese nodo.

   Carga el informe y muestra una tarjeta de resumen.

1. Haga clic en **[!UICONTROL Abrir informe]** para ver el informe completo.

**Consulta en lenguaje natural**

1. En el panel Compañero de trabajo, escriba una solicitud como _Dame el informe STO de [nombre de recorrido]_.

   El compañero interpreta la solicitud, carga la aptitud `send-time-report`, genera el informe y muestra una tarjeta de resumen.

1. Haga clic en **[!UICONTROL Abrir informe]** para ver el informe completo.

### Visualización de los datos del informe de correo electrónico {#sto-report-data}

Puede reducir el panel Compañero de trabajo para aumentar el tamaño del informe mostrado o desplazarse para ver el ancho completo.

![Informe de optimización del tiempo de envío: resumen del rendimiento del correo electrónico](./assets/email-sto-reporting-summary-report.png){width="700" zoomable="yes"}

En la columna _[!UICONTROL Detalles]_, haga clic en **[!UICONTROL Ver resultados de STO]** para abrir una ventana emergente. La ventana proporciona visualizaciones de datos de correo electrónico para _Comparación de rendimiento_, _Distribución del tiempo de envío_ e _Integridad de datos_.

![Informe de optimización del tiempo de envío: datos de rendimiento del correo electrónico](./assets/email-sto-reporting-data.png){width="500" zoomable="yes"}
