---
description: Supprime les utilisateurs d’un tableau de groupes.
seo-description: Supprime les utilisateurs d’un tableau de groupes.
seo-title: removeGroupMember
solution: Experience Manager
title: removeGroupMember
topic: Scene7 Image Production System API
uuid: 553d91a3-73d6-4323-9436-a3ba13260a6c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeGroupMember{#removegroupmembership}

Supprime les utilisateurs d’un tableau de groupes.

**Différences Entre Les Commandes De Suppression**

* `removeGroupMembers`: Supprime plusieurs utilisateurs d’un groupe.
* `removeGroupMembership`: Supprime un utilisateur individuel d’un tableau de groupes.

## Types d’utilisateurs autorisés {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Entrée (removeGroupMembshipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Non | Identifiant du dont vous souhaitez supprimer l’appartenance au groupe. |
| ` *`groupHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées vers des groupes à partir desquels vous souhaitez supprimer le. |

**Output (removeGroupMembshipReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-f8d4181170a243efb9faf5824ae96197}

Cet exemple de code supprime un utilisateur d’un groupe.

**Request**

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
