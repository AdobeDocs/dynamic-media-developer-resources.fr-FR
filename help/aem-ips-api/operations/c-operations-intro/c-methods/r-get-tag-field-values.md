---
description: Récupère toutes les valeurs du dictionnaire de balises définies pour un ou plusieurs champs de balises.
solution: Experience Manager
title: getTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 12836783-4f9d-41d3-9b42-6e25238d7ed5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 16%

---

# getTagFieldValues{#gettagfieldvalues}

Récupère toutes les valeurs du dictionnaire de balises définies pour un ou plusieurs champs de balises.

Syntaxe

## Types d’utilisateurs autorisés {#section-cc36a437394c491594e704a08a161c87}

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
| CompanyHandle | `xsd:string` | Oui | Pseudo de l’entreprise contenant le champ de balise. |
| Réseau de manipulation de champ | `types:HandleArray` | Oui | Tableau de poignées de champ permettant de renvoyer les valeurs que vous souhaitez renvoyer. |

**Output (getTagFieldValuesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Tableau de champs | `types:TagFieldValuesArray` | Oui | Tableau des valeurs de balise du dictionnaire pour chaque champ demandé. |

## Exemples {#section-4492742614e44bb191a7d397dc1a1407}

**Demander**

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
