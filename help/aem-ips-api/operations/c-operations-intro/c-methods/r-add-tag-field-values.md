---
description: Ajoute de nouvelles valeurs de balise au dictionnaire d’un champ de balise existant.
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 13%

---

# addTagFieldValues{#addtagfieldvalues}

Ajoute de nouvelles valeurs de balise au dictionnaire d’un champ de balise existant.

Syntaxe

## Types d’utilisateurs autorisés {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Entrée (addTagFieldValuesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Gestionnaire de la société contenant le champ de balise. |
| `*`fieldHandle`*` | `xsd:string` | Oui | Gestionnaire du champ de balise à modifier. |
| `*`valueArray`*` | `xsd:string` | Oui | Tableau de valeurs de balise à ajouter au dictionnaire existant du champ. |

**Sortie (addTagFieldValuesParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

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
