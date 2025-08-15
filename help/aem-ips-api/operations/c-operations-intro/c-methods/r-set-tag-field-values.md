---
description: Définit les valeurs du dictionnaire de balises pour un champ de balise existant.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 13%

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
| CompanyHandle | `xsd:string` | Oui | Pseudo de l’entreprise. |
| Poignée de champ | `xsd:string` | Oui | Poignée de champ de balise. |
| Tableau de valeurs | `types:StringArray` | Oui | Matrice de valeurs de balises qui remplace le dictionnaire existant du champ. Les associations d’actifs sont conservées lorsqu’une nouvelle valeur correspond à une valeur existante. |

**Output (setTagFieldValuesReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-b11cafd9bed54ab5836c737cc075c918}

**Demander**

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
