---
description: Ajoute de nouvelles valeurs de balise au dictionnaire d’un champ de balise existant.
solution: Experience Manager
title: addTagFieldValues
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 14%

---


# addTagFieldValues{#addtagfieldvalues}

Ajoute de nouvelles valeurs de balise au dictionnaire d’un champ de balise existant.

Syntaxe

## Types d’utilisateur autorisés {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Entrée (addTagFieldValuesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société contenant le champ de balise. |
| `*`fieldHandle`*` | `xsd:string` | Oui | Handle du champ de balise à modifier. |
| `*`valueArray`*` | `xsd:string` | Oui | Tableau de valeurs de balise à ajouter au dictionnaire existant du champ. |

**Output (addTagFieldValuesParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-c4049392f1c548f883b8b1f8f167bada}

**Request**

```java
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**Réponse**

Aucune
