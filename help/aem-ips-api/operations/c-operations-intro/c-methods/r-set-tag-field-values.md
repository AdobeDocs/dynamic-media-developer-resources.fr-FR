---
description: Définit les valeurs du dictionnaire de balises pour un champ de balise existant.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 15%

---

# setTagFieldValues{#settagfieldvalues}

Définit les valeurs du dictionnaire de balises pour un champ de balise existant.

Syntaxe

## Types d’utilisateurs autorisés {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-a05cbee4cb4f44198c414a6b14e69156}

**Entrée**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société. |
| `*`fieldHandle`*` | `xsd:string` | Oui | Poignée de champ de balise. |
| `*`valueArray`*` | `types:StringArray` | Oui | Tableau de valeurs de balise qui remplacent le dictionnaire existant du champ. Les associations de ressources sont conservées lorsqu’une nouvelle valeur correspond à une valeur existante. |

**Sortie (setTagFieldValuesReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-b11cafd9bed54ab5836c737cc075c918}

**Request**

```java
<setTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Nurth</items>
      <items>Suth</items>
      <items>East</items>
      <items>West</items>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</setTagFieldValuesParam>
```

**Réponse**

Aucune
