---
title: Permisos del producto
description: Lista de referencia de los permisos de Experience Platform que controlan el acceso a las funciones de Marketo Optimizer, con descripciones y permisos recomendados para los usuarios administradores, de acceso completo y de solo lectura.
TQID: https://experienceleague.adobe.com/Q4HnGxPkiE0dsZUjIgPvVJHgs0dPwLJiOKVSL1edS4Y
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3cf5f37e-e87e-5179-812b-53ce05d7eebb
    internal-label: Setup
  - id: a659ad61-de21-559d-a901-02e2fb329ff5
    internal-label: Administration
subfeature_v2:
  - id: b6434e31-d7bb-5416-960c-1c77bb1a2e8d
    internal-label: User Access
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
autotag-review: '2026-10-20T17:03:48.312Z'
source-git-commit: e80513284d179a9b27d0505463d07d5e15facabb
workflow-type: tm+mt
source-wordcount: '1577'
ht-degree: 3%
---
# Permisos de productos

Los siguientes permisos controlan el acceso a las características de [!DNL Adobe Marketo Optimizer]. Añádalos a los roles en el área de _[!UICONTROL Permisos]_ de [!DNL Adobe Experience Platform]. Para obtener información detallada sobre cómo crear funciones y asignarlas a los usuarios, consulte [_Acceso y permisos de usuario_](./user-management.md).

Las últimas tres columnas muestran los permisos recomendados para cada uno de los [tipos de usuarios sugeridos](#suggested-user-types): Administrador, Todos los usuarios de acceso y Usuario de acceso de solo lectura. Una marca de verificación (✔) significa que se recomienda el permiso para ese tipo de usuario, y un guión (-) significa que no lo es. Ajuste las recomendaciones para adaptarlas a su organización.

>[!IMPORTANT]
>
>El acceso a [!DNL Marketo Optimizer] requiere que habilite una zona protegida específica que esté aprovisionada con la siguiente convención de nombres: `Mktoaep` + prefijo de suscripción de [!DNL Marketo Engage]. Por ejemplo, si el prefijo de suscripción [!DNL Marketo Engage] vinculado es _AcmeAssoc_, la zona protegida necesaria para el acceso de [!DNL Marketo Optimizer] es _MktoaepAcmeAssoc_. Agregue esta zona protegida a cada función.

>[!NOTE]
>
>Debe ser administrador del sistema para ver el mosaico _[!UICONTROL Permisos]_ en Experience Platform.

Algunos permisos se aplican a funciones que aún no están disponibles en el producto. Los administradores pueden agregar estos permisos ahora para que los usuarios tengan el acceso aplicable cuando las funciones estén disponibles.

## Tipos de usuarios sugeridos {#suggested-user-types}

Utilice las recomendaciones de permisos de las tablas de esta página como punto de partida para las funciones que cree. Son sugerencias para cada tipo de usuario. Ajústelas para adaptarlas a su organización.

| Atributo | Administrador | Todos los usuarios de acceso | Usuario de acceso de solo lectura |
| --- | ----- | --------------- | --------------------- |
| **Para quién es** | Personas que configuraron y administraron [!DNL Marketo Optimizer] para su equipo. | Especialistas en marketing y operadores que trabajan en [!DNL Marketo Optimizer] todos los días. | Personas que necesitan ver [!DNL Marketo Optimizer] pero no cambiar nada, como ejecutivos, analistas y auditores. |
| **Qué pueden hacer** | Todo, incluidos los ajustes de configuración y administración. | Utilice todas las funciones: recorridos, programas, contenido, listas, informes y el asistente. | Vea recorridos, programas, contenido, listas e informes, y haga preguntas al asistente. |
| **Permisos para asignar** | Todos los permisos de esta página (seleccione **[!UICONTROL Agregar todos]** en el editor de funciones). | Los permisos con un ✔ en la columna _Todos los accesos_ de las tablas de esta página. | Los permisos con un ✔ en la columna _Solo lectura_ de las tablas de esta página. |
| **No incluido** | – | <li>Configuraciones de administración<li>Configuraciones de canal, incluida la configuración de correo electrónico, los ajustes preestablecidos de formulario, la configuración de página de aterrizaje y los ajustes preestablecidos de WhatsApp<li>Tipos de programas (ver y administrar) | <li>Creando, editando, eliminando, publicando o exportando (todos los permisos de _Administrar_ y _Publicar_, excepto el acceso de chat)<li>Activación de audiencias en destinos<li>Configuraciones de administración y configuración de canal, incluida la visualización de la configuración de correo electrónico y los ajustes preestablecidos de formulario<li>Visualización de tipos de programas |
| **Grupo de usuarios sugerido** | Grupo de administradores de Marketo Optimizer | Grupo de usuarios de Marketo Optimizer | Grupo de usuarios de solo lectura de Marketo Optimizer |
| **Función sugerida** | Administrador de Marketo Optimizer | Marketo Optimizer All Access User | Usuario de acceso de solo lectura de Marketo Optimizer |

Para ver el procedimiento para crear estos grupos y funciones, consulte [Crear grupos de usuarios y funciones para tipos de usuarios sugeridos](./user-management.md#create-suggested-roles).

## Contenido y recursos {#content-assets}

| Categoría | Permiso | Descripción | Administrador | Todos los accesos | Solo lectura |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Assets B2B | Administración de Assets B2B | Cree, edite y elimine archivos de recursos. | ✔ | ✔ | – |
| | Administración de correos electrónicos B2B | Crear, editar y eliminar mensajes de correo electrónico. | ✔ | ✔ | – |
| | Administración de Forms B2B | Crear, editar y eliminar formularios. | ✔ | ✔ | – |
| | Administrar fragmentos B2B | Crear, editar y eliminar fragmentos de contenido. | ✔ | ✔ | – |
| | Administrar página de aterrizaje B2B | Cree, edite y elimine páginas de aterrizaje. | ✔ | ✔ | – |
| | Administrar exportación de mensajes B2B | Exporte informes de mensajes en la sección _Correo electrónico_. | ✔ | ✔ | – |
| | Administrar plantillas B2B | Cree, edite y elimine plantillas de contenido. | ✔ | ✔ | – |
| | Gestionar seminarios web B2B | Cree, edite y elimine seminarios web interactivos. | ✔ | ✔ | – |
| | Publicar Forms B2B | Publicar formularios para utilizarlos en páginas de aterrizaje. | ✔ | ✔ | – |
| | Publicar fragmentos B2B | Publique fragmentos de contenido para utilizarlos en plantillas, correos electrónicos y páginas de aterrizaje. | ✔ | ✔ | – |
| | Publicar página de aterrizaje B2B | Publicar páginas de aterrizaje. | ✔ | ✔ | – |
| | Ver Assets B2B | Vea los detalles de la biblioteca Assets y el archivo de recursos. | ✔ | ✔ | ✔ |
| | Ver correos electrónicos B2B | Ver mensajes de correo electrónico. | ✔ | ✔ | ✔ |
| | Ver Forms B2B | Ver formularios. | ✔ | ✔ | ✔ |
| | Ver fragmentos B2B | Ver lista y detalles de fragmentos de contenido. | ✔ | ✔ | ✔ |
| | Ver página de aterrizaje de B2B | Ver páginas de aterrizaje. | ✔ | ✔ | ✔ |
| | Ver plantillas B2B | Ver lista y detalles de plantillas de contenido. | ✔ | ✔ | ✔ |
| | Ver seminarios web B2B | Ver seminarios web interactivos. | ✔ | ✔ | ✔ |

## Configuración y administración de canales {#channels-admin}

| Categoría | Permiso | Descripción | Administrador | Todos los accesos | Solo lectura |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Configuraciones de administración B2B | Administrar configuraciones de administración B2B | Configure las opciones de administración, como conexiones de administración de recursos digitales, repositorios de recursos y eventos. | ✔ | – | – |
| Configuraciones de canal B2B | Administrar configuraciones de canales B2B | Acceso al elemento de menú _Canales_ en la navegación izquierda y todas las operaciones de configuración de canal. | ✔ | – | – |
| | Administrar configuración de correo electrónico B2B | Configure las opciones de correo electrónico. Esta configuración es necesaria para que los usuarios puedan enviar correos electrónicos. | ✔ | – | – |
| | Administrar ajustes preestablecidos de Forms B2B | Cree, edite y elimine ajustes preestablecidos de formulario. | ✔ | – | – |
| | Administrar configuración de página de aterrizaje B2B | Configure la página de aterrizaje, como los subdominios. | ✔ | – | – |
| | Administrar ajustes preestablecidos de WhatsApp B2B | Cree, vea y elimine ajustes preestablecidos de mensajes de WhatsApp y ajustes de SMS asociados. | ✔ | – | – |
| | Administrar configuración de WhatsApp B2B | Configura los canales de WhatsApp. | ✔ | – | – |
| | Publicar ajuste preestablecido de Forms B2B | Publicar ajustes preestablecidos de formulario. | ✔ | – | – |
| | Ver configuración de correo electrónico B2B | Ver la configuración de correo electrónico (subdominios, registros PTR, grupos de IP, listas de supresión, listas de semilla, planes de calentamiento de IP). | ✔ | – | – |
| | Ver ajustes preestablecidos de Forms B2B | Ver ajustes preestablecidos de formulario. | ✔ | – | – |

## Recorridos, programas y carpetas {#journeys-programs}

| Categoría | Permiso | Descripción | Administrador | Todos los accesos | Solo lectura |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Tokens de carpeta B2B | Administrar tokens de carpeta B2B | Cree, edite y elimine tokens en carpetas. Los cambios se aplican a todo el contenido de la carpeta, por lo que debe asignarlos por separado de _Administrar carpetas B2B_. | ✔ | ✔ | – |
| | Ver tokens de carpeta B2B | Ver tokens definidos en carpetas. | ✔ | ✔ | ✔ |
| Carpetas B2B | Administrar carpetas B2B | Cree, edite y elimine carpetas. | ✔ | ✔ | – |
| | Ver carpetas B2B | Ver carpetas. | ✔ | ✔ | ✔ |
| Recorridos B2B | Administración del control de tráfico de Recorrido B2B | Configure el control de tráfico de recorrido, incluida la simulación de su efecto. | ✔ | ✔ | – |
| | Administrar Recorridos de persona B2B | Acceso a la lista _Recorridos de personas_ y a todas las operaciones de recorrido de personas. | ✔ | ✔ | – |
| | Publicar Recorridos de persona B2B | Publicar recorridos de persona. | ✔ | ✔ | – |
| | Ver control de tráfico de Recorrido B2B | Ver configuración de control de tráfico de recorrido. | ✔ | ✔ | ✔ |
| | Ver informes de Recorrido de personas B2B | Ver informes de recorrido de personas, incluido el informe _Persona de Recorrido_. | ✔ | ✔ | ✔ |
| | Ver Recorridos de persona B2B | Acceso de solo lectura a la lista de _Recorridos de personas_ y detalles del recorrido. | ✔ | ✔ | ✔ |
| Tokens de programa B2B | Administrar tokens de programa B2B | Cree, edite y elimine tokens en programas y tipos de programas. | ✔ | ✔ | – |
| | Ver tokens de programa B2B | Ver tokens definidos en programas y tipos de programas. | ✔ | ✔ | ✔ |
| Tipos de programas B2B | Administrar tipos de programas B2B | Cree, edite y elimine tipos de programas de marketing. | ✔ | – | – |
| | Ver tipos de programas B2B | Ver tipos de programas de marketing. | ✔ | – | – |
| Programas B2B | Administrar programas B2B | Cree, edite y elimine programas de marketing. | ✔ | ✔ | – |
| | Ver programas B2B | Ver programas de marketing. | ✔ | ✔ | ✔ |

## Audiencias, intención y destinos {#audiences-intent}

| Categoría | Permiso | Descripción | Administrador | Todos los accesos | Solo lectura |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Destinos B2B | Activar destinos B2B | Activar audiencias en destinos B2B. | ✔ | ✔ | – |
| | Administrar destinos B2B | Cree, edite y elimine destinos B2B. | ✔ | ✔ | – |
| | Ver destinos B2B | Acceso de solo lectura a destinos B2B. | ✔ | ✔ | ✔ |
| Configuración de intención B2B | Administrar configuración de intención B2B | Cree, edite y elimine configuraciones por intención. | ✔ | ✔ | – |
| | Ver configuración de intención B2B | Ver configuraciones por intención (modelos de ponderación por intención). | ✔ | ✔ | ✔ |
| Reglas de organización B2B | Administrar reglas de organización B2B | Cree, edite y elimine reglas de organización. | ✔ | ✔ | – |
| | Ver reglas de organización B2B | Ver reglas de organización. | ✔ | ✔ | ✔ |
| Listas de personas B2B | Administrar listas de personas B2B | Cree, edite y elimine listas de personas y administre la pertenencia a listas. | ✔ | ✔ | – |
| | Ver listas de personas B2B | Ver listas de personas estáticas y dinámicas. | ✔ | ✔ | ✔ |

## Informes, Labs y chat {#reports-labs-chat}

| Categoría | Permiso | Descripción | Administrador | Todos los accesos | Solo lectura |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Experiencia de conversación B2B | Administración de la experiencia de conversación B2B | Acceso al panel de chat y al asistente. Las acciones del panel también requieren el permiso de función coincidente. Por ejemplo, para crear un recorrido se requiere _Administrar Recorridos de persona B2B_. Consulte [Permisos de chat](#chat-permissions). | ✔ | ✔ | ✔ |
| Laboratorios B2B | Administración de B2B Labs | Habilite y configure las funciones de Labs. | ✔ | ✔ | – |
| | Ver laboratorios B2B | Vea las funciones de Labs disponibles y habilitadas. | ✔ | ✔ | ✔ |
| Informes B2B | Ver informes incrustados de B2B | Vea los informes en la ficha _Informes_. | ✔ | ✔ | ✔ |
| | Ver informes de intención B2B | Ver informes de intención. | ✔ | ✔ | ✔ |

## Permisos de chat {#chat-permissions}

Los permisos de chat siguen los permisos de nivel de funcionalidad. _Administrar experiencia de conversación B2B_ proporciona acceso al panel de chat de [!DNL CX Coworker], pero no concede acceso a ninguna función. El compañero comprueba cada habilidad o acción en el chat con el mismo permiso que necesita la función fuera del chat: _Administrar_ permisos para crear, editar o publicar y _Ver_ permisos para aptitudes de solo lectura. Si un usuario no tiene el permiso de característica, [!DNL Coworker] no podrá realizar esa acción. Por ejemplo, para crear un recorrido se requieren _Administrar Recorridos de persona B2B_, y para enumerar formularios se requiere _Ver Forms B2B_.

## Permisos de destinos externos {#external-destinations-permissions}

Para proporcionar acceso a destinos externos a los usuarios de [!DNL Marketo Optimizer], se requieren los siguientes permisos. Las columnas siguen las mismas recomendaciones para cada tipo de usuario descrito en [Tipos de usuarios sugeridos](#suggested-user-types).

| Categoría | Permiso | Descripción | Administrador | Todos los accesos | Solo lectura |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Paneles de control | Administrar paneles estándar | Agregue atributos personalizados que aún no estén en el almacén de datos. | ✔ | ✔ | – |
| | Ver paneles estándar | Acceso de solo vista a los paneles de _Perfiles_, _Destinos_ y _Segmentos_. También habilita el acceso a _Paneles_ en el panel de navegación izquierdo. | ✔ | ✔ | ✔ |
| Destinos | Activar destinos | Activar datos en destinos activos. También se requiere _Ver destinos_ o _Administrar destinos_. | ✔ | ✔ | – |
| | Activar segmento sin asignación | Activar audiencias en destinos existentes sin el paso de asignación. Los usuarios pueden agregar y eliminar audiencias en flujos de trabajo de activación, pero no pueden agregar ni eliminar atributos o identidades asignados. _Ver destinos_ también es obligatorio. | ✔ | ✔ | – |
| | Creación de destino | Destinos de autor que utilizan Experience Platform Destination SDK. | ✔ | ✔ | – |
| | Administrar y activar el destino del conjunto de datos | Vea, cree, edite y deshabilite flujos de exportación de conjuntos de datos y active datos para conjuntos de datos. _Ver destinos_ también es obligatorio. | ✔ | ✔ | – |
| | Administrar destinos | Ver, crear y eliminar destinos, conexiones y cuentas de destino. | ✔ | ✔ | – |
| | Ver destinos | Vea los destinos disponibles en la ficha _Catálogo_ y los destinos autenticados en la ficha _Examinar_. | ✔ | ✔ | ✔ |
| Gobernanza de datos | Administrar etiquetas de eliminación de uso B2B | Ver, crear y eliminar etiquetas de uso de datos (DULE) aplicadas a conjuntos de datos y esquemas. | ✔ | ✔ | – |
| | Administrar políticas de uso de datos | Ver, crear, editar y eliminar políticas de uso de datos. | ✔ | ✔ | – |
| | Ver directivas de uso de datos | Acceso de solo vista para políticas de uso de datos que pertenecen a su organización. | ✔ | ✔ | ✔ |
| Ingesta de datos | Administrar fuentes | Ver, crear, editar y deshabilitar orígenes. | ✔ | ✔ | – |
| | Ver orígenes | Vea los orígenes disponibles en la ficha _Catálogo_ y los orígenes autenticados en la ficha _Examinar_. | ✔ | ✔ | ✔ |
| Administración de perfiles | Administrar configuración de perfil | Ver y editar todas las configuraciones de perfil. | ✔ | ✔ | – |
| | Ver configuración del perfil | Acceso de solo vista a todas las configuraciones de perfil. | ✔ | ✔ | ✔ |

<!-- 

## Planned permissions {#planned-permissions}

The following permissions are for features that are not yet available in [!DNL Marketo Optimizer]. Adobe Marketo Qualifier permissions are not currently enforced. The estimated enforcement date is November 2026. Accounts and buying groups are targeted for delivery in Q1 2027.

| Category | Permission | Description | Admin | All Access | Read Only |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Marketo Qualifier Configurations | Manage Marketo Qualifier Configurations | Create, edit, and delete Marketo Qualifier configurations. | ✔ | – | – |
| | View Marketo Qualifier Configurations | View Marketo Qualifier configurations. | ✔ | ✔ | ✔ |
| Marketo Qualifier Outbound | View Marketo Qualifier Outbound | View Marketo Qualifier outbound workflows and outbound reporting. | ✔ | ✔ | ✔ |
| Marketo Qualifier Research | Manage Marketo Qualifier Research | Use and manage research capabilities. | ✔ | ✔ | – |
| | View Marketo Qualifier Research | View research: conversational interface, prospect view, and account and lead research. | ✔ | ✔ | ✔ |
| B2B Account Lists | Manage B2B Account Lists | Create, edit, and delete account lists, including adding, removing, and importing accounts. | ✔ | ✔ | – |
| B2B Buying Groups | Manage B2B Buying Groups | Create, edit, and delete buying groups. | ✔ | ✔ | – |
| | Manage B2B Role Templates | Manage the role templates used in buying groups. | ✔ | ✔ | – |
| | Manage B2B Solution Interests | Manage the solution interests used in buying groups. | ✔ | ✔ | – |
| | Manage B2B Stages | Manage buying group stages. | ✔ | ✔ | – |
| | View B2B Buying Groups | View buying groups. | ✔ | ✔ | ✔ |

-->
