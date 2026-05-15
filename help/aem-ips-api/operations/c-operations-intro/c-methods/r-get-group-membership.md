---
description: Renvoie les membres d’un groupe.
solution: Experience Manager
title: getGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 847e4982-219d-47fd-b94c-f7d520ba1367
TQID: 'https://experienceleague.adobe.com/V-LNnM0C56dTOos0qky91nxTLyBJMFxLt4VOD99nTN0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 17%

---

# getGroupMembership{#getgroupmembership}

Renvoie les membres d’un groupe.

Syntaxe

## Types d’utilisateurs autorisés {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-2e92f850254e46e48403acaa215341a5}

**Input (getGroupMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| userHandle | `xsd:string` | Non | Poignée de l’utilisateur. |
| companyHandle | `xsd:string` | Non | La poignée de la société. |

**Output (getGroupMembershipReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| groupArray | `types:GroupArray` | Oui | Tableau de groupes. |

## Exemples {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Cet exemple de code renvoie tous les membres d’un groupe. Les descripteurs d’entreprise et d’utilisateur étant facultatifs, l’opération peut renvoyer tous les membres de tous les groupes.

**Requête**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**Réponse**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```
