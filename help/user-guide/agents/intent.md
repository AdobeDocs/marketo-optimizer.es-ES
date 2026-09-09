---
title: Configurar y analizar intención
description: Obtenga información sobre cómo configurar las ponderaciones de actividad para el modelo de puntuación por intención y analizar la intención a nivel de posible cliente con informes de clasificación, perfil, tendencia y comparación.
source-git-commit: 8b3ea5f52fc50ea6c995ace44dece90247deff8b
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---


# Configuración y análisis de la intención

En [!DNL Adobe Marketo Optimizer], el compañero proporciona dos habilidades en la categoría _Intención_. Cada cliente valora las actividades de marketing de forma diferente, por lo que estas habilidades le permiten configurar lo que importa para su negocio. A continuación, puede validar lo que produjo la canalización por intención.

| Habilidad | Comando | Qué hace |
| --- | --- | --- |
| **Configuración por intención** | `/intent-configuration` (alias `/intent-config`) | Configurar las ponderaciones de actividad para el modelo de puntuación por intención de persona |
| **Analizar intención** | `/analyze-intent` | Consulte y valide informes de comparación, taxonomía de tendencias, productos y palabras clave y clasificación por intención de nivel de posible cliente |

Al seleccionar una habilidad, se inserta su descripción como un indicador de inicio en la entrada de conversación, que puede editar antes de enviar.

## Configuración del modelo de ponderación {#configure-model}

Para configurar las ponderaciones de actividad del modelo de puntuación por intención, siga estos pasos generales. Para obtener más información acerca de la configuración y la ponderación de puntuación, vea [_Configuración por intención_](../audiences/intent-configuration.md).

1. Invoque la aptitud (`/intent-configuration`) y presione **Intro**.

   El compañero abre el panel **[!UICONTROL Configuración por intención]** como una ficha del espacio de trabajo. El panel enumera todas las actividades de intención de la canalización, y muestra una puntuación de **[!UICONTROL AI sugerido]** y una puntuación de **[!UICONTROL Ponderación]** editables para cada una. También enumera los modelos que ya existen para el inquilino. Solo un modelo puede ser _[!UICONTROL Activo]_ en cualquier momento: el que administra la puntuación actualmente.

1. Para hacer cambios, abre un modelo _[!UICONTROL Borrador]_ existente o selecciona **[!UICONTROL Duplicado]** en el modelo _[!UICONTROL Activo]_ para comenzar desde sus pesos actuales.

1. Ajuste los pesos fila a fila.

   Por ejemplo, marca una actividad de bajo valor como **[!UICONTROL Agregar a oportunidad]** como **[!UICONTROL Trivial]** y aumenta **[!UICONTROL Haz clic en Enviar correo electrónico]** o en **[!UICONTROL Hacer clic en vínculo]** a **[!UICONTROL Importante]** si esas actividades importan más para tu negocio.

1. Seleccione **[!UICONTROL Guardar]**.

   Al guardar, se le pedirá que active el modelo ahora. Al confirmar, se reemplazará el modelo actual _[!UICONTROL Activo]_, el cual se degradará automáticamente.

## Puntuación por intención

La puntuación de intención de un posible cliente tiene en cuenta tres cosas:

* **Peso configurado aquí** para cada tipo de actividad.
* **Relevancia de contenido**: palabras clave extraídas de los recursos vinculados a cada actividad.
* **Frecuencia**: cuántas veces el posible cliente ha interactuado con ese contenido.

Para obtener detalles sobre estas métricas, incluido el peso sugerido por IA, la relevancia del contenido y las limitaciones, consulte [Configuración por intención](../audiences/intent-configuration.md).

## Informes de intención

Para presentar los cuatro tipos de informes que puede generar, invoque `/analyze-intent` para solicitar a Coworker. A continuación, el compañero espera una solicitud de seguimiento que especifica un posible cliente, un producto o una comparación. Cada informe se abre como su propia ficha en el panel del espacio de trabajo y el colaborador también agrega una tarjeta de resumen en el chat con un botón _[!UICONTROL Abrir informe]_.

### Informe Clasificación por intención

**Mensaje sugerido:** _&quot;Mostrar mis principales posibles clientes con intenciones altas para &lt;product>&quot;_

Clasifica los posibles clientes según la intensidad de la señal por intención de un producto o palabra clave. Las columnas incluyen posible cliente, correo electrónico, cuenta, sector, productos, puntuación, nivel de intención y el origen de la actividad principal. La columna _[!UICONTROL delta de 7 días]_ muestra cómo se ha movido la puntuación de intención en la última semana. La columna _[!UICONTROL Última actualización]_ muestra cuándo interactuó por última vez el posible cliente, es decir, cuándo cambió por última vez la puntuación. Los filtros para el producto y el nivel de intención son desplegables activos, por lo que no se limita a lo que escribió en el mensaje. Las columnas se pueden ordenar.

Otras solicitudes que abren el mismo informe:

* &quot;Clasifique los 10 posibles clientes principales por puntuación de intención para Photoshop&quot;
* &quot;Enumerar posibles clientes con alta intención para Photoshop&quot;
* &quot;Muéstrame posibles clientes cuya puntuación de intención para Photoshop haya sido la que más ha saltado esta semana&quot;
* &quot;Los posibles clientes del sector minorista muestran una intención de media a alta para Creative Cloud&quot;
* &quot;Buscar posibles clientes con puntuaciones de intención contribuidas por descargas de recursos en un seminario web&quot;
* &quot;Enumerar los posibles clientes con intención alta cuya principal fuente de actividad sea el clic en el correo electrónico&quot;
* &quot;Mostrar posibles clientes con la intención de contribuir solo con las visitas web, excluidas las descargas o los seminarios web&quot;

### Informe Perfil de intención

**Mensaje sugerido:** _&quot;Mostrarme el perfil de intención de &lt;lead>&quot;_

Una instantánea rápida de un posible cliente: qué productos y palabras clave muestran interés en y la puntuación de cada uno. Utilice este informe una vez que un informe de clasificación haya salido a la luz un posible cliente que merezca la pena investigar. Le ayuda a dar forma a recorridos, personalidades y grupos de compras en torno a la intención real del producto de ese posible cliente.

Otras indicaciones:

* &quot;¿En qué productos está más interesado &lt;lead>?&quot;
* &quot;¿Qué le interesa a &lt;lead> en este momento?&quot;
* &quot;Dame un resumen de todos los productos y las palabras clave que el posible cliente X ha mostrado intención para&quot;

### Informe Tendencia por intención

**Mensaje sugerido:** _&quot;Mostrar el historial de puntuación de intención de &lt;lead&#39;s> para &lt;product> en los últimos 30 días&quot;_

Traza la puntuación de intención de un posible cliente para un producto a lo largo del tiempo. Utilícela para identificar puntos de inflexión. Por ejemplo, una puntuación que permanece constante durante semanas y luego cae marcadamente indica un cambio en el interés, no datos irrelevantes. Puede ajustar el periodo de tiempo a 7, 30 o 100 días.

Otras indicaciones:

* &quot;¿Cuál es el pico de intención de Acrobat esta semana para el posible cliente X?&quot;
* &quot;Muéstrame la tendencia de intención para una pista este mes&quot;
* &quot;¿Ha subido o bajado este mes la intención del líder X para Acrobat?&quot;

### Informe de comparación por intención

**Mensaje sugerido:** _&quot;Compare tendencias por intención para Photoshop con Illustrator en todos los posibles clientes en los últimos 30 días&quot;_

Compara la intención con el tiempo para dos posibles clientes o dos productos, como un gráfico en paralelo más una tabla de resumen (puntuación actual, puntuación hace N días, delta). El intervalo de tiempo se puede ajustar del mismo modo que el informe de tendencias. La intención puede variar diariamente, minuto a minuto o por hora, por lo que una breve ventana plana no necesariamente significa que no esté pasando nada.

Otras indicaciones:

* &quot;Comparar la intención de Acrobat y Photoshop en el último trimestre&quot;
* &quot;Comparar la intención del posible cliente X con la del posible cliente Y para Creative Cloud&quot;
* &quot;¿Cuál tiene una intención promedio más alta: Photoshop o Illustrator?&quot;
* &quot;Comparar perfiles para Acrobat: ¿quién tiene la tasa de ganancia más alta?&quot;
* &quot;Mostrar la intención de Photoshop en paralelo en los segmentos minorista y financiero&quot;

## Seguimiento del informe {#report-follow-up}

Los informes por intención son de solo lectura y no tienen opción de exportación independiente. Para actuar según lo que muestra un informe, utilice otras habilidades en su lugar.

* Preguntar con _&quot;Enumerar los principales posibles clientes con intención de usar para Creative Cloud.&quot;_ El compañero utiliza la aptitud `/analyze-intent` para producir la lista especificada.

* Preguntar con _&quot;Crear una lista de personas con esta lista.&quot;_ El compañero entrega el conjunto de posibles clientes a [habilidad de creación de audiencias](./audience-creation.md), que crea la lista de personas directamente. No es necesario realizar ningún paso de exportación o importación manual.
