---
description: Renvoie des groupes de sociétés.
seo-description: Renvoie des groupes de sociétés.
seo-title: getGroups
solution: Experience Manager
title: getGroups
topic: Scene7 Image Production System API
uuid: d6e1542d-83a2-4b25-a986-2465e9e5a145
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 21%

---


# getGroups{#getgroups}

Renvoie des groupes de sociétés.

Syntaxe

## Types d’utilisateur autorisés {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-0e06195f23dd4c69922df210f566dd18}

**Entrée (getGroupsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | La poignée de la société. |

**Sortie (getGroupsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`groupArray`*` | `types:GroupArray` | Oui | Tableau de groupes. |

## Exemples {#section-ed0708f611574354bf0c6ea83912b531}

Ce code renvoie un tableau qui contient tous les groupes appartenant à une société spécifique et des informations spécifiques sur chaque groupe.

**Request**

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

