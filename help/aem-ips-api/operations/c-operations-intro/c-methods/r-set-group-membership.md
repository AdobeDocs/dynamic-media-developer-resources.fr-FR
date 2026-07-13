---
description: Définit l’appartenance à un groupe pour un utilisateur.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
TQID: 'https://experienceleague.adobe.com/j-wK2g-evSRY0YD3ZspgT--giCkKJl1VBYgPylixVz8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 11%

---

# setGroupMembership{#setgroupmembership}

Définit l’appartenance à un groupe pour un utilisateur.

Syntaxe

## Types d’utilisateurs autorisés {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Input (setGroupMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| userHandle | `xsd:string` | Non | Descripteur de l’utilisateur dont vous souhaitez définir l’appartenance à un groupe. |
| companyHandle | `xsd:string` | Non | Identifiant de la société. |
| groupHandleArray | `types:HandleArray` | Oui | Tableau des descripteurs des groupes auxquels l’utilisateur doit appartenir. |

**Output (setGroupMembershipReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-67b86d259df24938896fe19061845811}

Cet exemple de code fait de l’utilisateur un membre d’un groupe. Ajoutez un utilisateur à plusieurs groupes avec le tableau de gestion des groupes.

**Requête**

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

