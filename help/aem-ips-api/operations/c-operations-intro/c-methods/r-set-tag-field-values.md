---
description: Définit les valeurs du dictionnaire de balises pour un champ de balise existant.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
TQID: 'https://experienceleague.adobe.com/--ArL0CPejqbpJX-G7Z8zdU97WVXXjGfWc74UmOWSV0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
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
| companyHandle | `xsd:string` | Oui | Identifiant de la société. |
| fieldHandle | `xsd:string` | Oui | Identifiant du champ de balise. |
| valueArray | `types:StringArray` | Oui | Tableau de valeurs de balise qui remplacent le dictionnaire existant du champ. Les associations de ressources sont conservées lorsqu’une nouvelle valeur correspond à une valeur existante. |

**Output (setTagFieldValuesReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-b11cafd9bed54ab5836c737cc075c918}

**Requête**

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
