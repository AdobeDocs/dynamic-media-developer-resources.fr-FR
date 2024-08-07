---
description: Renvoie les groupes d’entreprises.
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d98c08a6-4c20-4538-9598-c905078ab7de
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 21%

---

# getGroups{#getgroups}

Renvoie les groupes d’entreprises.

Syntaxe

## Types d’utilisateurs autorisés {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-0e06195f23dd4c69922df210f566dd18}

**Entrée (getGroupsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | La poignée de la société. |

**Sortie (getGroupsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| groupArray | `types:GroupArray` | Oui | Tableau de groupes. |

## Exemples {#section-ed0708f611574354bf0c6ea83912b531}

Ce code renvoie un tableau qui contient tous les groupes appartenant à une société spécifique et des informations spécifiques sur chaque groupe.

**Requête**

```java
<ns1:getGroupsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupsParam>
```

```java
<getGroupsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle>
         <companyHandle>47</companyHandle>
         <name>MyGroup</name>
         <isSystemDefined>false</isSystemDefined>
      </items>
   </groupArray>
</getGroupsReturn>
```
