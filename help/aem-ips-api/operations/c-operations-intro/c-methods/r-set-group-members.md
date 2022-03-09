---
description: Définit l’appartenance à un groupe d’utilisateurs appartenant à une société spécifique.
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 9%

---

# setGroupMembers{#setgroupmembers}

Définit l’appartenance à un groupe d’utilisateurs appartenant à une société spécifique.

L’opération renvoie une erreur d’authentification si vous ne disposez pas des privilèges nécessaires pour effectuer cette opération. C’est également le cas si l’un des utilisateurs du tableau de pseudo n’appartient pas à la société spécifiée dans le nom de l’entreprise,

## Types d’utilisateurs autorisés {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-6a18562fc8e942af94be10bbb8c51151}

**Entrée (setGroupMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Poignée de la société. |
| groupHandle | `xsd:string` | Oui | Poignée de groupe. |
| userHandleArray | `types:HandleArray` | Oui | Tableau de poignées pour les utilisateurs dont vous souhaitez définir l’appartenance à un groupe. |

**Sortie (setGroupMembesReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-9c528c3f44a141ce9eaddf634f26c487}

Cet exemple de code définit l’appartenance à un groupe pour un utilisateur unique.

**Request**

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
