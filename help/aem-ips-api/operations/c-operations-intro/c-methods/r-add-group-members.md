---
description: Ajoute des utilisateurs d’une société spécifique à un groupe spécifique.
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 12%

---

# addGroupMembers{#addgroupmembers}

Ajoute des utilisateurs d’une société spécifique à un groupe spécifique.

Syntaxe

## Types d’utilisateurs autorisés {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-b28434dcf2ca4b4ea431136aac33913e}

**Entrée (addGroupMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | La poignée de la société. |
| `*`groupHandle`*` | `xsd:string` | Oui | Le gestionnaire du groupe. |
| `*`userHandleArray`*` | `types:HandleArray` | Oui | Tableau de gestionnaires destinés aux utilisateurs que vous souhaitez ajouter à un groupe. |

**Sortie (addGroupMembersParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-8f168b528aef4c4fa8c3d41f7686842f}

Cet exemple utilise `*`addGroupMembersParam`*` pour ajouter un utilisateur à une seule société. L’API IPS ne renvoie pas de réponse pour cette opération.

**Request**

```java
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**Réponse**

Aucune
