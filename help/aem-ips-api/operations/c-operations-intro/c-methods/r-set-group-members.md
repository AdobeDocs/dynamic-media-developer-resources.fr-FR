---
description: Définit l’appartenance au groupe des utilisateurs appartenant à une société spécifique.
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 7%

---

# setGroupMembers{#setgroupmembers}

Définit l’appartenance au groupe des utilisateurs appartenant à une société spécifique.

L’opération génère une erreur d’authentification si vous ne disposez pas des privilèges pour effectuer cette opération. Cela est également vrai si l’un des utilisateurs du tableau de descripteurs d’utilisateur n’appartient pas à la société spécifiée dans le descripteur de société,

## Types d’utilisateurs autorisés {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-6a18562fc8e942af94be10bbb8c51151}

**Input (setGroupMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Pseudo de l’entreprise. |
| Poignée de groupe | `xsd:string` | Oui | Nom de groupe. |
| userHandleArray | `types:HandleArray` | Oui | Tableau de poignées pour les utilisateurs dont vous souhaitez définir l’appartenance au groupe. |

**Output (setGroupMembesReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-9c528c3f44a141ce9eaddf634f26c487}

Cet exemple de code définit l’appartenance à un groupe pour un seul utilisateur.

**Demander**

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
