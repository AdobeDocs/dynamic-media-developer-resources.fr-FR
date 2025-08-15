---
description: Un type de jeu de propriétés spécifie différents paramètres utilisés pour aider à gérer les jeux de propriétés.
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 10%

---

# createPropertySetType{#createpropertysettype}

Un type de jeu de propriétés spécifie différents paramètres utilisés pour aider à gérer les jeux de propriétés.

Syntaxe

## Types d’utilisateurs autorisés {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-43dece72eb9f44df80f4a119dd2c008b}

**Input (createPropertySetTypeParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Non | Identifiant de la société propriétaire du type de jeu de propriétés. Si `companyHandle` n’est pas transmis et que l’appelant est un `IpsAdmin`, un type de jeu de propriétés global est créé. |
| nom | `xsd:string` | Oui | Nom du type de jeu de propriétés. |
| propertyType | `xsd:string` | Oui | Choix des types de jeux de propriétés. |
| allowMultiple | `xsd:boolean` | Oui | Détermine si votre programme peut avoir plusieurs jeux de propriétés. |

**Output (createPropertySetTypeReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| typeHandle | `xsd:string` | Oui | Poignée au type. |

## Exemples {#section-13396c9639a6475190e622eae3cdb534}

Cet exemple de code crée un jeu de propriétés avec un nom et un type spécifiés par la constante `PropertySet Types`. Identifiant de la société propriétaire du type de jeu de propriétés. Si companyHandle n’est pas transmis et que l’appelant est un IpsAdmin, un type de jeu de propriétés global est créé.

**Requête**

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
