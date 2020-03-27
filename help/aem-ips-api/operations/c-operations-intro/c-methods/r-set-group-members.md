---
description: Définit l’appartenance au groupe des utilisateurs appartenant à un  de spécifique.
seo-description: Définit l’appartenance au groupe des utilisateurs appartenant à un  de spécifique.
seo-title: setGroupMembers
solution: Experience Manager
title: setGroupMembers
topic: Scene7 Image Production System API
uuid: fe6585ef-a4b3-4b3c-95d0-624017650497
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setGroupMembers{#setgroupmembers}

Définit l’appartenance au groupe des utilisateurs appartenant à un  de spécifique.

L’opération renvoie une erreur d’authentification si vous ne disposez pas des privilèges nécessaires pour effectuer cette opération. Cela est également vrai si l’un des utilisateurs du tableau des pseudo-utilisateurs n’appartient pas au  de spécifié dans le  de poignée du,

## Types d’utilisateurs autorisés {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-6a18562fc8e942af94be10bbb8c51151}

**Input (setGroupMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui |  poignée. |
| ` *`groupHandle`*` | `xsd:string` | Oui | Poignée du groupe. |
| ` *`userHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées pour les utilisateurs dont vous souhaitez définir l’appartenance au groupe. |

**Output (setGroupMembesReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

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
