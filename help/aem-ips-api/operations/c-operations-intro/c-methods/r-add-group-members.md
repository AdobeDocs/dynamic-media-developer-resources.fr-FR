---
description: Ajoute les utilisateurs d’une société spécifique à un groupe spécifique.
solution: Experience Manager
title: addGroupMembers
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 12%

---


# addGroupMembers{#addgroupmembers}

Ajoute les utilisateurs d’une société spécifique à un groupe spécifique.

Syntaxe

## Types d’utilisateur autorisés {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-b28434dcf2ca4b4ea431136aac33913e}

**Entrée (addGroupMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | La poignée de la société. |
| `*`groupHandle`*` | `xsd:string` | Oui | Handle du groupe. |
| `*`userHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées destinées aux utilisateurs que vous souhaitez ajouter à un groupe. |

**Output (addGroupMembersParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-8f168b528aef4c4fa8c3d41f7686842f}

Cet exemple utilise `*`addGroupMembersParam`*` pour ajouter un utilisateur à une seule société. L&#39;API IPS ne renvoie pas de réponse pour cette opération.

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
