---
description: Supprime les valeurs de champ de balise du dictionnaire d’un champ de balise.
seo-description: Supprime les valeurs de champ de balise du dictionnaire d’un champ de balise.
seo-title: deleteTagFieldValues
solution: Experience Manager
title: deleteTagFieldValues
topic: Dynamic Media Image Production System API
uuid: 71cdec4e-c1d6-4518-87ed-5c47a5112b15
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 12%

---


# deleteTagFieldValues{#deletetagfieldvalues}

Supprime les valeurs de champ de balise du dictionnaire d’un champ de balise.

## Types d’utilisateur autorisés {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-5db64a6ae238426395bc760b83587260}

**Entrée (deleteTagFieldValuesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société contenant le champ de balise. |
| `*`fieldHandle`*` | `xsd:string` | Oui | Handle du champ de balise à modifier. |
| `*`valueArray`*` | `types:StringArray` | Oui | Tableau de valeurs de balise à supprimer du dictionnaire du champ. |

**Output (deleteTagFieldValuesParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-92f9e575a6da491caa09e264b4d6ee55}

**Request**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**Réponse**

Aucune
