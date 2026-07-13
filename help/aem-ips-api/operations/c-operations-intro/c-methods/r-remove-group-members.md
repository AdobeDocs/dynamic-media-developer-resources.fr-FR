---
description: Supprime les utilisateurs de l’entreprise d’un groupe spécifique.
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
TQID: 'https://experienceleague.adobe.com/dMEOhQgXQvFvZj2Kozsq6J7qJNiwYpknQQbNkADMsg0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 8%

---

# removeGroupMembers{#removegroupmembers}

Supprime les utilisateurs de l’entreprise d’un groupe spécifique.

**Différences Entre Les Commandes De Suppression**

* `removeGroupMembers` : supprime plusieurs utilisateurs d’un groupe.
* `removeGroupMembership` : supprime un utilisateur individuel d’un tableau de groupes.

## Types d’utilisateurs autorisés {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-b5596614a3be4ce5962455884e4636af}

**Input (removeGroupMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | La poignée de la société avec les utilisateurs avec lesquels vous souhaitez travailler. |
| groupHandle | `xsd:string` | Oui | Identifiant du groupe. |
| userHandleArray | `types:HandleArray` | Oui | Tableau d’identifiants pour les utilisateurs dont vous souhaitez supprimer les appartenances à des groupes. |

**Output (removeGroupMembersParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-9eedac852cea46ec80de6a6928bf97ac}

Cet exemple de code supprime un utilisateur de la société spécifiée. Supprimez plusieurs utilisateurs d’un groupe avec le tableau de gestion des utilisateurs.

**Requête**

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**Réponse**

Aucune

