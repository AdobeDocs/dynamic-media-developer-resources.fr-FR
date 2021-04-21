---
description: Définit les valeurs du dictionnaire de balises pour un champ de balise existant.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 14%

---


# setTagFieldValues{#settagfieldvalues}

Définit les valeurs du dictionnaire de balises pour un champ de balise existant.

Syntaxe

## Types d’utilisateur autorisés {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-a05cbee4cb4f44198c414a6b14e69156}

**Entrée**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de société. |
| `*`fieldHandle`*` | `xsd:string` | Oui | Poignée de champ de balise. |
| `*`valueArray`*` | `types:StringArray` | Oui | Tableau de valeurs de balise qui remplacent le dictionnaire existant du champ. Les associations d’actifs sont conservées lorsqu’une nouvelle valeur correspond à une valeur existante. |

**Output (setTagFieldValuesReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

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
