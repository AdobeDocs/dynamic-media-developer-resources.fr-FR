---
description: Obtient les utilisateurs qui appartiennent à une société et un groupe spécifiques.
seo-description: Obtient les utilisateurs qui appartiennent à une société et un groupe spécifiques.
seo-title: getGroupMembers
solution: Experience Manager
title: getGroupMembers
topic: Dynamic Media Image Production System API
uuid: 02322b66-1c0c-4d84-a3eb-97a4fb605318
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 16%

---


# getGroupMembers{#getgroupmembers}

Obtient les utilisateurs qui appartiennent à une société et un groupe spécifiques.

Syntaxe

## Types d’utilisateur autorisés {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-b798b06354c946abbb90fa72cc9c67fd}

**Entrée (getGroupMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | La poignée de la société. |
| `*`groupHandle`*` | `xsd:string` |  | Poignée du groupe. |

**Output (getGroupMembersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`userHandleArray`*` | `type:HandleArray` | Oui | Tableau de poignées utilisateur. |

## Exemples {#section-aaa340dba6b64cce9bcd8303cf999166}

Cet exemple de code renvoie un tableau d&#39;utilisateur contenant tous les utilisateurs appartenant à un groupe spécifique.

**Request**

```java
<ns1:getGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
</ns1:getGroupMembersParam>
```

**Réponse**

```java
<getGroupMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userHandleArray>
      <items>70|kmagnusson@adobe.com</items>
   </userHandleArray>
</getGroupMembersReturn>
```

