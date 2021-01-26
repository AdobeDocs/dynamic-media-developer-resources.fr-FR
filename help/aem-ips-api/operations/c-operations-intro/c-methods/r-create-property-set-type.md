---
description: Un type de jeu de propriétés spécifie divers paramètres utilisés pour aider à gérer les jeux de propriétés.
seo-description: Un type de jeu de propriétés spécifie divers paramètres utilisés pour aider à gérer les jeux de propriétés.
seo-title: createPropertySetType
solution: Experience Manager
title: createPropertySetType
topic: Dynamic Media Image Production System API
uuid: ecbaad48-d725-4f7a-a37d-5e4cde3295cb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 11%

---


# createPropertySetType{#createpropertysettype}

Un type de jeu de propriétés spécifie divers paramètres utilisés pour aider à gérer les jeux de propriétés.

Syntaxe

## Types d’utilisateur autorisés {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-43dece72eb9f44df80f4a119dd2c008b}

**Entrée (createPropertySetTypeParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Non | Poignée de la société propriétaire du type de jeu de propriétés. Si `companyHandle` n&#39;est pas transmis et que l&#39;appelant est un `IpsAdmin`, un type de jeu de propriétés global est créé. |
| `*`name`*` | `xsd:string` | Oui | Nom du type de jeu de propriétés. |
| `*`propertyType`*` | `xsd:string` | Oui | Choix des types de jeux de propriétés. |
| `*`allowMultiple`*` | `xsd:boolean` | Oui | Détermine si votre programme peut comporter plusieurs jeux de propriétés. |

**Output (createPropertySetTypeReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Oui | Poignée du type. |

## Exemples {#section-13396c9639a6475190e622eae3cdb534}

Cet exemple de code crée un jeu de propriétés avec un nom et un type spécifiés par la constante `PropertySet Types`. Poignée de la société propriétaire du type de jeu de propriétés. Si companyHandle n’est pas transmis et que l’appelant est un IpsAdmin, un type de jeu de propriétés global est créé.

**Request**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10803</typeHandle>
</createPropertySetTypeReturn>
```

**Réponse**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</createPropertySetTypeReturn>
```

