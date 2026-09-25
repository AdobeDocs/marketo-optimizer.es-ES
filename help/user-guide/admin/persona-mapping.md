---
title: Asignación de personas
description: Obtenga información sobre cómo configurar la asignación de personalidades en Marketo Optimizer. Asigne atributos de persona para definir personas y utilice el filtrado Persona derivada en listas de personas y recorridos de personas.
TQID: 'https://experienceleague.adobe.com/JCBtJN4DgQZROVDamM4eKuCiGTwJQPQY3wMxmBPFj74'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 46e599c6-e20f-5f67-9824-93415016f66b
    internal-label: Audiences
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
    internal-label: Journeys
  - id: a659ad61-de21-559d-a901-02e2fb329ff5
    internal-label: Administration
  - id: d4203578-d294-5145-b397-f26f4488a904
    internal-label: Channels
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: fd79d458ef033e4485ba5e8a8c8fbe56b7cd559b
workflow-type: tm+mt
source-wordcount: '1287'
ht-degree: 1%
---
# Asignación de persona

Las personas son un aspecto clave de un enfoque de marketing basado en cuentas (ABM), ya que ayudan a los especialistas en marketing a ajustar sus estrategias a las necesidades, preferencias y puntos problemáticos específicos de las personas dentro de las cuentas de destino. Los especialistas en marketing pueden crear perfiles detallados para cada persona, incluidos sus antecedentes, responsabilidades, puntos problemáticos y canales de comunicación preferidos. Con estas definiciones, los administradores pueden configurar los perfiles según los atributos de la persona en [!DNL Adobe Marketo Optimizer] para que las listas de personas y los recorridos de personas puedan utilizar un filtrado simplificado y coherente que capture a estos perfiles.

En [!DNL Marketo Optimizer], la asignación de personas proporciona una capacidad adicional que va más allá de las condiciones de la plantilla de rol: puede filtrar [listas de personas](../audiences/people-lists.md) y [recorridos de personas](../marketing/person-journeys.md) utilizando **[!UICONTROL Persona derivada]** como criterio de filtro. Una persona _derivada_ es la persona que el sistema infiere para un registro de persona mediante la evaluación de sus atributos en relación con todas las definiciones de persona configuradas.

Limitaciones de uso y definición personal:

* Puede tener hasta 20 personalidades definidas en la lista _[!UICONTROL Asignación personal]_.
* Cada persona puede incluir hasta cinco atributos en su definición.
* En todas las personalidades definidas, puede utilizar hasta diez atributos de persona diferentes.

>[!BEGINSHADEBOX]

**Caso de uso: variaciones del puesto**

Muchos equipos de marketing y ventas utilizan los puestos como una forma de identificar diferentes personas dentro de una cuenta. Sin embargo, los títulos de los contactos pueden ser incoherentes y utilizar numerosas variaciones para funciones similares. Al crear filtros de lista de personas o condiciones de audiencia de recorrido de personas, es posible que tenga que definir todos los posibles títulos de trabajo relacionados para una función determinada. Puede simplificar estas definiciones y agrupar a las personas con títulos de trabajo similares en una persona deducida, a la cual puede destinar filtrando _Persona derivada es liderazgo_ en lugar de hacer coincidir valores de títulos de trabajo individuales.

>[!ENDSHADEBOX]

## Acceso a los perfiles configurados {#access}

Abra el panel _Asignación personal_ desde la [interfaz de chat](../agents/chat-interface.md) de Coworker.

1. En el panel de chat, escriba `/persona-mapping` y presione **Intro**.

   Este comando es un acceso directo de navegación, mostrado en **[!UICONTROL Abrir una página]** en el menú de barra.

   ![Captura de pantalla del menú de barra de la interfaz de chat que muestra el comando /persona-mapping en Abrir una página.](assets/persona-mapping-open-chat.png){width="800" zoomable="yes"}

1. El compañero abre el panel **[!UICONTROL Asignación de personalidades]** como una ficha del espacio de trabajo, donde se muestra la lista de personalidades.

   Desde este panel, puedes [crear](#create-a-persona), [editar](#edit-a-persona) o [eliminar](#delete-a-persona) personalidades.

   La lista de personas está organizada como una tabla que muestra cada nombre de persona, fecha de creación y fecha de última modificación. <!-- You can customize the displayed table by clicking the _Column settings_ ( ![Column settings](../assets/do-not-localize/icon-column-settings.svg) ) icon in the top-right corner and selecting or clearing the column checkboxes. --> Puede minimizar el panel de chat para aumentar el tamaño del panel _Asignación personal_.

   ![Panel de asignación de personalidades que muestra una tabla de personalidades predeterminadas y un botón Crear personalidad.](assets/persona-mapping-list.png){width="700" zoomable="yes"}

1. Para acceder a los detalles de una persona, haga clic en el nombre.

### Personalidades predeterminadas

La lista _Asignación de personalidades_ incluye diez personalidades predeterminadas que se definen según el atributo del cargo. Puede editar cualquiera de estos perfiles predeterminados según las necesidades de su organización:

| Persona | Títulos de trabajo |
| ------- | ---------- |
| CXO/EVP | CEO, CIO, CTO, CMO, CFO, Vicepresidente Ejecutivo de Estrategia |
| VP/VP | vicepresidente senior de marketing, vicepresidente de ventas, vicepresidente de operaciones, vicepresidente de producto, vicepresidente de TI |
| Director/director sénior | Director de Ingeniería, Director de Producto, Director de Finanzas, Director de Éxito del Cliente |
| Responsable sénior/responsable | Director de Marketing, Director de TI, Director de Operaciones, Director de Ventas, Director de Recursos Humanos |
| Colaborador individual | Ejecutivo de cuentas, Ingeniero de software, Especialista en marketing, Representante de éxito del cliente |
| Analista | Analista de negocios, Analista de datos, Analista de investigación de mercado, Analista financiero, Analista de operaciones |
| Desarrollador | Desarrollador front-end, desarrollador back-end, desarrollador de pila completa, desarrollador de aplicaciones móviles, ingeniero de DevOps |
| Personal del cuadro orgánico | Especialista en Recursos Humanos, Asesor Jurídico, Oficial de Cumplimiento, Gerente de Proyectos, Especialista en Adquisiciones |
| Consultor | Consultor de administración, consultor de TI, consultor de procesos empresariales, consultor de marketing |
| Otro | Especialista en el sector, Asesor independiente, Consultor independiente, Experto en la materia |

### Filtrado de listas

Para localizar el perfil que desea, escriba una cadena de texto en la barra de búsqueda para que coincida con los perfiles por nombre.

![Campo de búsqueda que filtra la lista de personas por nombre y muestra dos resultados coincidentes.](assets/configuration-persona-mapping-search.png){width="680" zoomable="yes"}

## Crear una persona {#create-a-persona}

1. Haga clic en **[!UICONTROL Crear persona]**.

1. Escriba un **[!UICONTROL Nombre]** y una **[!UICONTROL Descripción]** únicos (opcionales) para la persona.

   ![Cree un panel de personalidad con campos Nombre y Descripción y una sección Reglas para seleccionar atributos.](assets/configuration-persona-mapping-new.png){width="680" zoomable="yes"}

1. Para **[!UICONTROL reglas]**, seleccione los atributos que se usarán para hacer coincidir la persona.

   * Haga clic en **[!UICONTROL Editar reglas]**.

   * En el cuadro de diálogo, seleccione la casilla de verificación de cada atributo que desee asignar (un máximo de cinco).

     Puede personalizar la tabla mostrada haciendo clic en el icono _Configuración de columna_ ( ![Configuración de columna](../assets/do-not-localize/icon-column-settings.svg) ) en la esquina superior derecha.

     Para filtrar la lista de atributos por nombre, introduzca una cadena de texto en la barra de búsqueda. También puede hacer clic en el icono _Filtro_ ( ![Icono de filtro](../assets/do-not-localize/icon-filter.svg) ) en la parte superior izquierda para filtrar la lista mostrada por tipo, _Estándar_ o _Personalizado_.

     ![Cuadro de diálogo que enumera atributos de persona con casillas de verificación, estado de uso y columnas de tipo de atributo.](assets/configuration-persona-mapping-select-attributes.png){width="450" zoomable="yes"}

   * Haga clic en **[!UICONTROL Finalizado]**.

     Los atributos seleccionados se rellenan en la sección _[!UICONTROL Atributos personales]_.

   * Para cada atributo, introduzca los valores separados por comas que desee que coincidan con el atributo.

1. Haga clic en **[!UICONTROL Crear persona]**.

## Editar una persona {#edit-a-persona}

Haga clic en el nombre de la persona para acceder y editar sus detalles.

Puede cambiar el nombre o la descripción, agregar atributos o actualizar los valores de los atributos. Haga clic en **[!UICONTROL Enviar]** cuando se hayan completado los cambios.

## Eliminar una persona {#delete-a-persona}

Al eliminar una persona, esta se eliminará de la lista _Asignación de personas_ y ya no estará disponible como filtro de persona derivado en las listas de personas o los recorridos de personas.

1. En la página _[!UICONTROL Asignación personal]_, busque el perfil que desee eliminar.

1. Junto al nombre, haga clic en los puntos suspensivos (**...**) y elija **[!UICONTROL Eliminar]**.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.

## Filtrar por persona derivada {#derived-persona-filter}

Una vez configuradas las personas, [!DNL Marketo Optimizer] deriva una persona para cada registro de persona mediante la evaluación de los atributos del registro frente a las asignaciones de personas definidas. Puede utilizar el resultado deducido (el _Persona derivada_) como filtro al definir la audiencia para una lista de personas o un recorrido de personas.

El filtro de Persona derivada aparece en el panel de filtros en la categoría **[!UICONTROL Atributos de persona]** junto con otros atributos deducidos, como la pertenencia a recorridos.

### Listas de personas

Para dirigirse a las personas que coincidan con un perfil configurado específico al administrar listas de personas, puede filtrar por Persona derivada.

**Lista estática — Agregar miembros**

1. Abra la lista estática y haga clic en **[!UICONTROL Agregar personas]** en la parte superior derecha.

1. En el cuadro de diálogo de filtro, expanda **[!UICONTROL Atributos de persona]** y arrastre **[!UICONTROL Persona derivada]** al lienzo.

   También puede introducir el nombre del filtro en el campo de búsqueda para localizarlo rápidamente.

   ![Filtro de Persona derivada agregado al lienzo de filtro de lista de personas con opciones de persona que se pueden seleccionar.](assets/persona-mapping-derived-persona-filter.png){width="680" zoomable="yes"}

1. En la condición de filtro, elija **[!UICONTROL is]** y seleccione una o más personalidades de la lista.

1. Haga clic en **[!UICONTROL Listo]** para aplicar el filtro y calificar a las personas coincidentes en la lista.

**Lista dinámica — Establecer reglas de pertenencia**

1. Abra la lista dinámica y seleccione la ficha **[!UICONTROL Reglas]**.

1. Haga clic en **[!UICONTROL Editar reglas]**.

1. En el cuadro de diálogo de filtro, expanda **[!UICONTROL Atributos de persona]** y arrastre **[!UICONTROL Persona derivada]** al lienzo.

   También puede introducir el nombre del filtro en el campo de búsqueda para localizarlo rápidamente.

1. En la condición de filtro, elija **[!UICONTROL is]** y seleccione una o más personalidades de la lista.

1. Haga clic en **[!UICONTROL Listo]** para guardar la regla.

   La pertenencia se actualiza automáticamente a medida que se evalúan los registros de persona según la regla.

### Recorridos de persona

Al configurar la audiencia para un recorrido de persona mediante una audiencia de evento, puede utilizar Personalidad derivada como un filtro de perfil de persona para controlar qué personas entran en el recorrido.

1. Haga clic en el nodo **[!UICONTROL Audiencia de personas]** en el lienzo del recorrido.

1. En el panel de propiedades del nodo, seleccione **[!UICONTROL Audiencia de evento]** como tipo de audiencia.

1. En **[!UICONTROL Filtros de perfil de persona]**, haga clic en **[!UICONTROL Agregar filtro]**.

1. Expanda **[!UICONTROL Atributos de persona]** y arrastre **[!UICONTROL Persona derivada]** al lienzo del filtro.

   También puede introducir el nombre del filtro en el campo de búsqueda para localizarlo rápidamente.

   ![Se ha agregado el filtro de Persona derivada a un lienzo de filtro de audiencia de evento de recorrido de persona.](assets/persona-mapping-derived-persona-event-filter.png){width="680" zoomable="yes"}

1. En la condición de filtro, elija **[!UICONTROL is]** y seleccione una o más personalidades de la lista.

   Solo las personas cuya personalidad derivada coincida con los valores seleccionados pueden entrar en el recorrido.

1. Haga clic en **[!UICONTROL Guardar]** para guardar los criterios del evento.
