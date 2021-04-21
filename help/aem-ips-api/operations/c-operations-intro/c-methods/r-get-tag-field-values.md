---
description: Récupère toutes les valeurs du dictionnaire de balises définies pour un ou plusieurs champs de balise.
solution: Experience Manager
title: getTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 17%

---


# getTagFieldValues{#gettagfieldvalues}

Récupère toutes les valeurs du dictionnaire de balises définies pour un ou plusieurs champs de balise.

Syntaxe

## Types d’utilisateur autorisés {#section-cc36a437394c491594e704a08a161c87}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-9ad806e7736e4d51ae42cad185050cf9}

**Entrée (getTagFieldValuesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société contenant le champ de balise. |
| `*`fieldHandleArray`*` | `types:HandleArray` | Oui | Un tableau de champs traite les valeurs de balise que vous souhaitez renvoyer. |

**Output (getTagFieldValuesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`fieldArray`*` | `types:TagFieldValuesArray` | Oui | Tableau des valeurs de balise dans le dictionnaire pour chaque champ demandé. |

## Exemples {#section-4492742614e44bb191a7d397dc1a1407}

**Request**

```java
<getTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandleArray>
      <items>m|3|ASSET|SingleOpenTag</items>
      <items>m|3|ASSET|SingleFixedTag</items>
   </fieldHandleArray>
</getTagFieldValuesParam>
```

**Réponse**

```java
<getTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <fieldArray>
      <items>
         <fieldHandle>m|3|ASSET|SingleOpenTag</fieldHandle>
         <valueArray>
            <items>GroupB</items>
            <items>GroupA</items>
         </valueArray>
      </items>
      <items>
         <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
         <valueArray>
            <items>North</items>
            <items>South</items>
            <items>East</items><items>West</items>
         </valueArray>
      </items>
   </fieldArray>
</getTagFieldValuesReturn>
```

