---
description: Condition de recherche de champ système pour l’opération searchAssets.
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
TQID: 'https://experienceleague.adobe.com/dCZl4pLGuG5hHpEq04W-qv8mRWcFiA7PvmzcO7Un-sM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 6%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

Condition de recherche de champ système pour l’opération searchAssets.

Pour les comparaisons unaires, transmettez exactement une valeur ( `boolVal`, `longVal`, `doubleVal` ou `dateVal`) en fonction du type de champ système. Pour les plages de recherche, transmettez les paramètres `min<Type>` et `max<Type>` et transmettez une valeur `op` de `Between` ou `NotBetween`.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| champ | `xsd:string` | Choix des champs système de recherche de ressources. |
| op | `xsd:string` | Choix des opérateurs de comparaison de chaînes. |
| valeur | `xsd:string` | Valeur en fonction de laquelle tester. |
| boolVal | `xsd:boolean` | Valeur de comparaison booléenne. |
| longVal | `xsd:long` | Valeur de comparaison longue. |
| minLong | `xsd:long` | Limite inférieure de longue portée. |
| maxLong | `xsd:long` | Limite supérieure de longue portée. |
| doubleVal | `xsd:double` | Valeur de comparaison double. |
| minDouble | `xsd:double` | Limite inférieure de la double plage. |
| maxDouble | `xsd:double` | Limite supérieure de la plage double. |
| dateVal | `xsd:dateTime` | Valeur de comparaison de dates. |
| minDate | `xsd:dateTime` | Période minimale. |
| maxDate | `xsd:dateTime` | Période maximale. |

## Exemple {#section-347d4aabfff44530adba03d1dc0b9968}

```
<systemFieldConditionArray>
   <items>
      <field>LastModified</field>
      <op>Between</op>
      <minDate>2007-08-01T00:00:00</minDate>
      <maxDate>2007-12-01T00:00:00</maxDate>
   </items>
</systemFieldConditionArray>
```

