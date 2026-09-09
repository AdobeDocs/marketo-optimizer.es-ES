---
title: Configurar lista de comprobación
description: Complete las tareas de configuración iniciales de la instancia de Marketo Optimizer, incluida la configuración de acceso de los usuarios y la infraestructura de envío de correo electrónico.
TQID: 'https://experienceleague.adobe.com/XEPKIa88-L7mdPz1opKegY1pdEF4Qyls0nLVJBQSaJk'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 3cf5f37e-e87e-5179-812b-53ce05d7eebbid: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 249
ht-degree: 10%

---

# Configurar lista de comprobación

Complete estas tareas para habilitar la funcionalidad en la instancia [!DNL Marketo Optimizer] aprovisionada.

## Habilitar acceso de usuario {#enable-user-access}

Cuando el aprovisionamiento se haya completado y las zonas protegidas estén enlazadas, configure el acceso de [!DNL Journey Optimizer B2B Edition] para su equipo y para los usuarios.

<table>
<thead>
<tr>
<th colspan="2">Tarea</th>
<th>Detalles e instrucciones</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Proporcionar acceso al producto y permisos</strong> para los usuarios</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Crear un perfil de producto de Journey Optimizer B2B edition en Admin Console (solo una vez/configuración inicial)</td>
<td><a href="./user-management.md#create-profile">Crear perfil</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Añadir un grupo de usuarios en Admin Console</td>
<td><a href="./user-management.md#add-user-group">Agregar grupo de usuarios</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Asigne el perfil de producto al grupo de usuarios en Admin Console</td>
<td><a href="./user-management.md#assign-profile">Asignar perfil de producto</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Añadir usuarios al grupo de usuarios en Admin Console</td>
<td><a href="./user-management.md#add-users">Añadir usuarios</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Editar funciones integradas o crear una función personalizada con permisos de producto</td>
<td><a href="./user-management.md#edit-role-permissions">Editar roles</a> <br/> <a href="./user-management.md#create-a-custom-role">Crear un rol personalizado</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Adición de usuarios o grupos a las funciones de Adobe Experience Platform</td>
<td><a href="./user-management.md#add-users-to-a-role">Agregar usuarios</a> <br/><a href="./user-management.md#add-user-groups-to-a-role">Agregar grupos</a></td>
</tr>
</tbody>
</table>

## Entregabilidad del correo electrónico {#email-deliverability}

Para que los especialistas en marketing puedan enviar correos electrónicos desde las recorridos, configure la infraestructura de envío de su organización, incluida la delegación de subdominios, la autenticación de correo electrónico y la configuración de canal.

<table>
<thead>
<tr>
<th colspan="2">Tarea</th>
<th>Detalles e instrucciones</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configuración de la entrega de correo electrónico y canales</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Delegación de un subdominio en Adobe (completamente delegado o CNAME)</td>
<td><a href="./email-deliverability.md#delegate-fully-delegated">Delegado completamente</a> <br/> <a href="./email-deliverability.md#delegate-cname">CNAME</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Configuración de DMARC para el subdominio</td>
<td><a href="./email-deliverability.md#configure-dmarc">Configuración de DMARC</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Revisar y asignar un grupo de IP</td>
<td><a href="./email-deliverability.md#review-ip-pool">Revisar grupo de IP</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Crear una configuración de canal de correo electrónico</td>
<td><a href="../admin/email-channel-configuration.md#create-email-channel-configuration">Configuración de canal de correo electrónico</a></td>
</tr>
</tbody>
