---
description: Définit l’appartenance à un groupe pour un utilisateur.
seo-description: Définit l’appartenance à un groupe pour un utilisateur.
seo-title: setGroupMembership
solution: Experience Manager
title: setGroupMembership
uuid: 3285fab0-92e4-4b88-9a3c-88cbb97d48c9
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 11%

---


# setGroupMembership{#setgroupmembership}

Définit l’appartenance à un groupe pour un utilisateur.

Syntaxe

## Types d’utilisateur autorisés {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Entrée (setGroupMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Non | Nom d’utilisateur dont vous souhaitez définir l’appartenance au groupe. |
| `*`companyHandle`*` | `xsd:string` | Non | Poignée de société. |
| `*`groupHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées effectuées sur des groupes auxquels appartient l’utilisateur. |

**Output (setGroupMembershipReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-67b86d259df24938896fe19061845811}

Cet exemple de code fait de l’utilisateur un membre d’un groupe. Ajoutez un utilisateur à plusieurs groupes à l’aide du tableau de descripteurs de groupe.

**Request**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**Réponse**

Aucune
