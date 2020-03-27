---
description: Supprime  utilisateurs d’un groupe spécifique.
seo-description: Supprime  utilisateurs d’un groupe spécifique.
seo-title: removeGroupMembers
solution: Experience Manager
title: removeGroupMembers
topic: Scene7 Image Production System API
uuid: dd0ea335-bbd0-43b1-830b-77f32dc39b12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeGroupMembers{#removegroupmembers}

Supprime  utilisateurs d’un groupe spécifique.

**Différences Entre Les Commandes De Suppression**

* `removeGroupMembers`: Supprime plusieurs utilisateurs d’un groupe.
* `removeGroupMembership`: Supprime un utilisateur individuel d’un tableau de groupes.

## Types d’utilisateurs autorisés {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-b5596614a3be4ce5962455884e4636af}

**Input (removeGroupMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | La poignée du avec les utilisateurs avec lesquels vous souhaitez travailler. |
| ` *`groupHandle`*` | `xsd:string` | Oui | Poignée du groupe. |
| ` *`userHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées pour les utilisateurs dont vous souhaitez supprimer les membres de groupe. |

**Output (removeGroupMembersParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-9eedac852cea46ec80de6a6928bf97ac}

Cet exemple de code supprime un utilisateur du  de spécifié. Supprimez plusieurs utilisateurs d’un groupe à l’aide du tableau d’identifiants utilisateur.

**Request**

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
