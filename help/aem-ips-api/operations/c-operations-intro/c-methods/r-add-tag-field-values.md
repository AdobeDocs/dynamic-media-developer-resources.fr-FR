---
description: Ajoute de nouvelles valeurs de balise au dictionnaire d’un champ de balise existant.
seo-description: Ajoute de nouvelles valeurs de balise au dictionnaire d’un champ de balise existant.
seo-title: addTagFieldValues
solution: Experience Manager
title: addTagFieldValues
topic: Scene7 Image Production System API
uuid: 9304f02c-a1df-4477-ab33-f2491c390c92
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addTagFieldValues{#addtagfieldvalues}

Ajoute de nouvelles valeurs de balise au dictionnaire d’un champ de balise existant.

Syntaxe

## Types d’utilisateurs autorisés {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Input (addTagFieldValuesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | poignée du contenant le champ de balise. |
| ` *`fieldHandle`*` | `xsd:string` | Oui | Poignée du champ de balise à modifier. |
| ` *`valueArray`*` | `xsd:string` | Oui | Tableau de valeurs de balise à ajouter au dictionnaire existant du champ. |

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
