---
description: Définit les valeurs du dictionnaire de balises pour un champ de balise existant.
seo-description: Définit les valeurs du dictionnaire de balises pour un champ de balise existant.
seo-title: setTagFieldValues
solution: Experience Manager
title: setTagFieldValues
topic: Scene7 Image Production System API
uuid: 56666c00-3694-4a43-a0ff-97af45c8df9f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Oui |  poignée. |
| ` *`fieldHandle`*` | `xsd:string` | Oui | Poignée de champ de balise. |
| ` *`valueArray`*` | `types:StringArray` | Oui | Tableau de valeurs de balise qui remplace le dictionnaire existant du champ. Les associations de ressources sont conservées lorsqu’une nouvelle valeur correspond à une valeur existante. |

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
