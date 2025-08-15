---
description: Supprime les valeurs de champ de balise du dictionnaire d’un champ de balise.
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 11%

---

# deleteTagFieldValues{#deletetagfieldvalues}

Supprime les valeurs de champ de balise du dictionnaire d’un champ de balise.

## Types d’utilisateurs autorisés {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-5db64a6ae238426395bc760b83587260}

**Entrée (deleteTagFieldValuesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Pseudo de l’entreprise contenant le champ de balise. |
| Poignée de champ | `xsd:string` | Oui | Poignée du champ de balise à modifier. |
| Tableau de valeurs | `types:StringArray` | Oui | Tableau de valeurs de balise à supprimer du dictionnaire du champ. |

**Output (deleteTagFieldValuesParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-92f9e575a6da491caa09e264b4d6ee55}

**Demander**

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
