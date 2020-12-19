---
description: Ajoute les utilisateurs d’une société spécifique à un groupe spécifique.
seo-description: Ajoute les utilisateurs d’une société spécifique à un groupe spécifique.
seo-title: addGroupMembers
solution: Experience Manager
title: addGroupMembers
topic: Scene7 Image Production System API
uuid: 382d36a8-7c93-48e6-a54b-425c5e6414fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 11%

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
| ` *`companyHandle`*` | `xsd:string` | Oui | La poignée de la société. |
| ` *`groupHandle`*` | `xsd:string` | Oui | Handle du groupe. |
| ` *`userHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées destinées aux utilisateurs que vous souhaitez ajouter à un groupe. |

**Output (addGroupMembersParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-8f168b528aef4c4fa8c3d41f7686842f}

Cet exemple utilise ` *`addGroupMembersParam`*` pour ajouter un utilisateur à une seule société. L&#39;API IPS ne renvoie pas de réponse pour cette opération.

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
