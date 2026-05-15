---
description: Supprime des utilisateurs d’un tableau de groupes.
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 892ee01c-e07b-4321-b0b7-5bb606036340
TQID: 'https://experienceleague.adobe.com/-RTuwtlTpQdiS-H-lf9BhQwbkp5McXo4tbxssF-0wzo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 8%

---

# removeGroupMembership{#removegroupmembership}

Supprime des utilisateurs d’un tableau de groupes.

**Différences Entre Les Commandes De Suppression**

* `removeGroupMembers` : supprime plusieurs utilisateurs d’un groupe.
* `removeGroupMembership` : supprime un utilisateur individuel d’un tableau de groupes.

## Types d’utilisateurs autorisés {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Input (removeGroupMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| userHandle | `xsd:string` | Non | Identifiant de la société dont vous souhaitez supprimer l’appartenance à un groupe. |
| groupHandleArray | `types:HandleArray` | Oui | Tableau de handles vers les groupes desquels vous souhaitez supprimer la société. |

**Output (removeGroupMembershipReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-f8d4181170a243efb9faf5824ae96197}

Cet exemple de code supprime un utilisateur d’un groupe.

**Requête**

```java
<ns1:removeGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>47</ns1:userHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:removeGroupMembershipParam>
```

**Réponse**

Aucune
