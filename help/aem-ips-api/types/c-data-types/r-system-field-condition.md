---
description: Condition de recherche de champ système pour l'opération searchAssets.
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# SystemFieldCondition{#systemfieldcondition}

Condition de recherche de champ système pour l&#39;opération searchAssets.

Pour les comparaisons unaires, transmettez exactement une valeur ( `boolVal`, `longVal`, `doubleVal` ou `dateVal`) en fonction du type de champ système. Pour les plages de recherche, transmettez les paramètres `min<Type>` et `max<Type>` et transmettez une valeur `op` de `Between` ou `NotBetween`.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`champ`*` | `xsd:string` | Choix des champs du système de recherche de ressources. |
| `*`op`*` | `xsd:string` | Choix des opérateurs de comparaison de chaînes. |
| `*`value`*` | `xsd:string` | Valeur à tester. |
| `*`boolVal`*` | `xsd:boolean` | Valeur de comparaison booléenne. |
| `*`longVal`*` | `xsd:long` | Valeur de comparaison longue. |
| `*`minLong`*` | `xsd:long` | Limite inférieure de la longue plage. |
| `*`maxLong`*` | `xsd:long` | Limite supérieure de la longue plage. |
| `*`doubleVal`*` | `xsd:double` | Valeur de comparaison du doublon. |
| `*`minDouble`*` | `xsd:double` | Limite inférieure de la plage de doublons. |
| `*`maxDouble`*` | `xsd:double` | Limite supérieure de la plage de doublons. |
| `*`dateVal`*` | `xsd:dateTime` | Valeur de comparaison de dates. |
| `*`minDate`*` | `xsd:dateTime` | Plage de dates minimale. |
| `*`maxDate`*` | `xsd:dateTime` | Plage de dates maximale. |

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

