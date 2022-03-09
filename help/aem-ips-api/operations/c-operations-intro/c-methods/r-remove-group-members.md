---
description: Supprime les utilisateurs de l’entreprise d’un groupe spécifique.
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 10%

---

# removeGroupMembers{#removegroupmembers}

Supprime les utilisateurs de l’entreprise d’un groupe spécifique.

**Différences entre les commandes de suppression**

* `removeGroupMembers`: Supprime plusieurs utilisateurs d’un groupe.
* `removeGroupMembership`: Supprime un utilisateur individuel d’un tableau de groupes.

## Types d’utilisateurs autorisés {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-b5596614a3be4ce5962455884e4636af}

**Entrée (removeGroupMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestionnaire de l’entreprise avec les utilisateurs avec lesquels vous souhaitez travailler. |
| groupHandle | `xsd:string` | Oui | Poignée de groupe. |
| userHandleArray | `types:HandleArray` | Oui | Tableau de gestionnaires pour les utilisateurs dont vous souhaitez supprimer des appartenances à un groupe. |

**Sortie (removeGroupMembersParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-9eedac852cea46ec80de6a6928bf97ac}

Cet exemple de code supprime un utilisateur de la société spécifiée. Supprimez plusieurs utilisateurs d’un groupe avec le tableau de gestion des utilisateurs.

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
