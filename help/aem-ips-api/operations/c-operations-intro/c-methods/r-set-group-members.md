---
description: Définit l’appartenance à un groupe d’utilisateurs appartenant à une société spécifique.
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
TQID: 'https://experienceleague.adobe.com/9gCJ-UKUNZI3AbQ0LFkxNUSS-w7bnG0FQE8SQeM2MMQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 7%

---

# setGroupMembers{#setgroupmembers}

Définit l’appartenance à un groupe d’utilisateurs appartenant à une société spécifique.

L’opération génère une erreur d’authentification si vous ne disposez pas des privilèges nécessaires pour accomplir cette opération. C’est également vrai si l’un des utilisateurs du tableau d’identifiants d’utilisateur n’appartient pas à la société spécifiée dans l’identifiant d’entreprise,

## Types d’utilisateurs autorisés {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-6a18562fc8e942af94be10bbb8c51151}

**Input (setGroupMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société. |
| groupHandle | `xsd:string` | Oui | Identifiant du groupe. |
| userHandleArray | `types:HandleArray` | Oui | Tableau de handles pour les utilisateurs dont vous souhaitez définir l’appartenance à un groupe. |

**Output (setGroupMembesReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-9c528c3f44a141ce9eaddf634f26c487}

Cet exemple de code définit l’appartenance à un groupe pour un seul utilisateur.

**Requête**

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**Réponse**

Aucune
