---
description: Obtient les utilisateurs appartenant à une société et à un groupe spécifiques.
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 18%

---

# getGroupMembers{#getgroupmembers}

Obtient les utilisateurs appartenant à une société et à un groupe spécifiques.

Syntaxe

## Types d’utilisateurs autorisés {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-b798b06354c946abbb90fa72cc9c67fd}

**Entrée (getGroupMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | La poignée de la société. |
| groupHandle | `xsd:string` |  | La poignée du groupe. |

**Sortie (getGroupMembersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| userHandleArray | `type:HandleArray` | Oui | Tableau de gestionnaires d’utilisateurs. |

## Exemples {#section-aaa340dba6b64cce9bcd8303cf999166}

Cet exemple de code renvoie un tableau de pseudo utilisateur contenant tous les utilisateurs appartenant à un groupe spécifique.

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
