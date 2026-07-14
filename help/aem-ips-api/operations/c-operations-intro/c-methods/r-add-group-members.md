---
description: Ajoute des utilisateurs d’une entreprise spécifique à un groupe spécifique.
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
TQID: 'https://experienceleague.adobe.com/iwy99zQOP-peI6mJgDE8bp7NGN6bjH1g5MBN53gIkJw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 10%

---

# addGroupMembers{#addgroupmembers}

Ajoute des utilisateurs d’une entreprise spécifique à un groupe spécifique.

Syntaxe

## Types d’utilisateurs autorisés {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-b28434dcf2ca4b4ea431136aac33913e}

**Input (addGroupMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | La poignée de la société. |
| groupHandle | `xsd:string` | Oui | Identifiant du groupe. |
| userHandleArray | `types:HandleArray` | Oui | Tableau d’identifiants pour les utilisateurs que vous souhaitez ajouter à un groupe. |

**Output (addGroupMembersParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-8f168b528aef4c4fa8c3d41f7686842f}

Cet exemple utilise addGroupMembersParam pour ajouter un utilisateur à une seule société. L’API IPS ne renvoie pas de réponse pour cette opération.

**Requête**

```java {.line-numbers}
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**Réponse**

Aucune

