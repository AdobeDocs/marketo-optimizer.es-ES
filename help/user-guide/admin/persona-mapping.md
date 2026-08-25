---
title: Asignación de personas
description: Obtenga información sobre cómo configurar la asignación de personas en Marketo Optimizer. Asigne atributos de persona para definir personas y utilice el filtrado Persona derivada en listas de personas y recorridos de personas.
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: '1216'
ht-degree: 1%

---

# Asignación de persona

<!-- not available until GA -->

Las personas son un aspecto clave de un enfoque de marketing basado en cuentas (ABM), ya que ayudan a los especialistas en marketing a ajustar sus estrategias a las necesidades, preferencias y puntos problemáticos específicos de las personas dentro de las cuentas de destino. Los especialistas en marketing pueden crear perfiles detallados para cada persona, incluidos sus antecedentes, responsabilidades, puntos problemáticos y canales de comunicación preferidos. Con estas definiciones, los administradores pueden configurar los perfiles según los atributos de la persona en Marketo Optimizer para que las listas de personas y los recorridos de personas puedan utilizar un filtrado optimizado y coherente que capture estos perfiles.

En Marketo Optimizer, la asignación de personas proporciona una capacidad adicional que va más allá de las condiciones de la plantilla de funciones: puede filtrar [listas de personas](../audiences/people-lists.md) y [recorridos de personas](../marketing/person-journeys.md) utilizando **[!UICONTROL Persona derivada]** como criterio de filtro. Una persona _derivada_ es la persona que el sistema infiere para un registro de persona mediante la evaluación de sus atributos en relación con todas las definiciones de persona configuradas.

Limitaciones de uso y definición personal:

* Puede tener hasta 20 personalidades definidas en la lista _[!UICONTROL Asignación personal]_.
* Cada persona puede incluir hasta cinco atributos en su definición.
* En todas las personalidades definidas, puede utilizar hasta diez atributos de persona diferentes.

>[!BEGINSHADEBOX]

**Caso de uso: variaciones del puesto**

Muchos equipos de marketing y ventas utilizan los puestos como una forma de identificar diferentes personas dentro de una cuenta. Sin embargo, los títulos de los contactos pueden ser incoherentes y utilizar numerosas variaciones para funciones similares. Al crear filtros de lista de personas o condiciones de audiencia de recorrido de personas, puede requerir que defina todos los posibles títulos de trabajo relacionados para una función determinada. Puede simplificar estas definiciones y colocar a las personas con títulos de trabajo similares en una sola persona deducida, a la que puede destinar filtrando _La persona derivada es la administración de productos_ en lugar de hacer coincidir los valores de los títulos de los trabajos individuales.

>[!ENDSHADEBOX]

## Acceso a los perfiles configurados {#access}

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Configuraciones]**.

1. Haga clic en **[!UICONTROL Asignación de personalidades]** en el panel intermedio para mostrar la lista de personalidades.

   ![Acceder a los perfiles configurados](assets/configuration-persona-mapping.png){width="800" zoomable="yes"}

   Desde esta página, puedes [crear](#create-a-persona), [editar](#edit-a-persona) o [eliminar](#delete-a-persona) personalidades.

   La lista de asignación Persona está organizada en forma de tabla y muestra los perfiles actualizados más recientemente en la parte superior (ordenados por _[!UICONTROL Última actualización]_). Puede personalizar la tabla mostrada si hace clic en el icono _Configuración de columna_ ( ![Configuración de columna](../assets/do-not-localize/icon-column-settings.svg) ) en la esquina superior derecha y activa o desactiva las casillas de verificación de la columna.

   ![Columnas para mostrar en la lista de asignación de personas](assets/configuration-persona-mapping-list-columns.png){width="300"}

1. Para acceder a los detalles de una persona, haga clic en el nombre.

### Personalidades predeterminadas

La lista _Asignación de personalidades_ incluye cinco personalidades predeterminadas que se definen según el atributo del puesto. Puede editar cualquiera de estos perfiles predeterminados según las necesidades de su organización:

| Persona | Títulos de trabajo |
| ------- | ---------- |
| CXO / EVP - CXO / Vicepresidente ejecutivo | CEO, CIO, CTO, CMO, CFO, Vicepresidente Ejecutivo de Estrategia |
| SVP / VP - Vicepresidente senior / Vicepresidente | vicepresidente senior de marketing, vicepresidente de ventas, vicepresidente de operaciones, vicepresidente de producto, vicepresidente de TI |
| Director Senior / Director - Director Senior / Director | Director de Ingeniería, Director de Producto, Director de Finanzas, Director de Éxito del Cliente |
| Responsable / Responsable - Responsable / Responsable | Director de Marketing, Director de TI, Director de Operaciones, Director de Ventas, Director de Recursos Humanos |
| Colaborador individual: colaborador individual | Ejecutivo de cuentas, Ingeniero de software, Especialista en marketing, Representante de éxito del cliente |
| Analista - Analista | Analista de negocios, Analista de datos, Analista de investigación de mercado, Analista financiero, Analista de operaciones |
| Desarrollador - Desarrollador | Desarrollador front-end, desarrollador back-end, desarrollador de pila completa, desarrollador de aplicaciones móviles, ingeniero de DevOps |
| Personal profesional - Personal profesional | Especialista en Recursos Humanos, Asesor Jurídico, Oficial de Cumplimiento, Gerente de Proyectos, Especialista en Adquisiciones |
| Consultor - Consultor | Consultor de administración, consultor de TI, consultor de procesos empresariales, consultor de marketing |
| Otros - Otros | Especialista en el sector, Asesor independiente, Consultor independiente, Experto en la materia |

### Filtrado de listas

Para localizar el perfil que desea, escriba una cadena de texto en la barra de búsqueda para que coincida con los perfiles por nombre.

![Filtrar las asignaciones de personas mostradas](assets/configuration-persona-mapping-search.png){width="700" zoomable="yes"}

## Crear una persona {#create-a-persona}

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Configuración]**.

1. Haga clic en **[!UICONTROL Asignación personal]** en el panel intermedio.

1. Haga clic en **[!UICONTROL Crear persona]**.

1. Escriba un **[!UICONTROL Nombre]** y una **[!UICONTROL Descripción]** únicos (opcionales) para la persona.

   ![Crear una asignación de persona](assets/configuration-persona-mapping-new.png){width="700" zoomable="yes"}

1. Seleccione los atributos que se utilizarán para hacer coincidir la persona.

   * Haga clic en **[!UICONTROL Seleccionar atributos de persona]**.

   * En el cuadro de diálogo, seleccione la casilla de verificación de cada atributo que desee asignar (un máximo de cinco).

     Puede personalizar la tabla mostrada haciendo clic en el icono _Configuración de columna_ ( ![Configuración de columna](../assets/do-not-localize/icon-column-settings.svg) ) en la esquina superior derecha.

     Para filtrar la lista de atributos por nombre, introduzca una cadena de texto en la barra de búsqueda. También puede hacer clic en el icono _Filtro_ ( ![Icono de filtro](../assets/do-not-localize/icon-filter.svg) ) en la parte superior izquierda para filtrar la lista mostrada por tipo, _Estándar_ o _Personalizado_.

     ![Cuadro de diálogo Seleccionar atributos de persona](assets/configuration-persona-mapping-select-attributes.png){width="700" zoomable="yes"}

   * Haga clic en **[!UICONTROL Guardar]**.

     Los atributos seleccionados se rellenan en la sección _[!UICONTROL Atributos personales]_.

1. Para cada atributo, introduzca los valores separados por comas que desee que coincidan con el atributo.

1. Haga clic en **[!UICONTROL Enviar]**.

## Editar una persona {#edit-a-persona}

Haga clic en el nombre de la persona para acceder y editar sus detalles.

Puede cambiar el nombre o la descripción, agregar atributos o actualizar los valores de los atributos. Haga clic en **[!UICONTROL Enviar]** cuando se hayan completado los cambios.

## Eliminar una persona {#delete-a-persona}

Al eliminar una persona, esta se eliminará de la lista _Asignación de personas_ y ya no estará disponible como filtro de persona derivado en las listas de personas o los recorridos de personas.

1. En la página _[!UICONTROL Asignación personal]_, busque el perfil que desee eliminar.

1. Junto al nombre, haga clic en los puntos suspensivos (**...**) y elija **[!UICONTROL Eliminar]**.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.

## Filtrar por persona derivada {#derived-persona-filter}

Una vez configuradas las personas, Marketo Optimizer deriva una persona para cada registro de persona mediante la evaluación de los atributos del registro respecto a las asignaciones de personas definidas. Puede utilizar el resultado deducido (el _Persona derivada_) como filtro al definir la audiencia para una lista de personas o un recorrido de personas.

El filtro de Persona derivada aparece en el panel de filtros en la categoría **[!UICONTROL Filtros especiales]** junto con otros atributos deducidos, como la pertenencia a recorridos.

### Listas de personas

Al agregar o quitar miembros de una lista de personas estática o al definir las reglas de pertenencia para una lista de personas dinámica, puede filtrar por Persona derivada para dirigirse a todas las personas cuyos atributos coincidan con una persona configurada específica.

**Lista estática — Agregar miembros**

1. Abra la lista estática y haga clic en **[!UICONTROL Agregar personas]** en la parte superior derecha.

1. En el cuadro de diálogo de filtro, expanda **[!UICONTROL Filtros especiales]** y arrastre **[!UICONTROL Persona derivada]** al lienzo.

1. En la condición de filtro, elija **[!UICONTROL is]** y seleccione una o más personalidades de la lista.

1. Haga clic en **[!UICONTROL Listo]** para aplicar el filtro y calificar a las personas coincidentes en la lista.

**Lista dinámica — Establecer reglas de pertenencia**

1. Abra la lista dinámica y seleccione la ficha **[!UICONTROL Reglas]**.

1. Haga clic en **[!UICONTROL Editar reglas]**.

1. En el cuadro de diálogo de filtro, expanda **[!UICONTROL Filtros especiales]** y arrastre **[!UICONTROL Persona derivada]** al lienzo.

1. En la condición de filtro, elija **[!UICONTROL is]** y seleccione una o más personalidades de la lista.

1. Haga clic en **[!UICONTROL Listo]** para guardar la regla.

   La pertenencia se actualiza automáticamente a medida que se evalúan los registros de persona según la regla.

### Recorridos de persona

Al configurar la audiencia para un recorrido de persona mediante una audiencia de evento, puede utilizar Personalidad derivada como un filtro de perfil de persona para controlar qué personas entran en el recorrido.

1. Haga clic en el nodo **[!UICONTROL Audiencia de personas]** en el lienzo del recorrido.

1. En el panel de propiedades del nodo, seleccione **[!UICONTROL Audiencia de evento]** como tipo de audiencia.

1. En **[!UICONTROL Filtros de perfil de persona]**, haga clic en **[!UICONTROL Agregar filtro]**.

1. Expanda **[!UICONTROL Filtros especiales]** y arrastre **[!UICONTROL Persona derivada]** al lienzo del filtro.

1. En la condición de filtro, elija **[!UICONTROL is]** y seleccione una o más personalidades de la lista.

   Solo las personas cuya personalidad derivada coincida con los valores seleccionados pueden entrar en el recorrido.
