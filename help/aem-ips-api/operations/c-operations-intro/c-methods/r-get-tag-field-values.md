---
description: Obtient toutes les valeurs du dictionnaire de balises définies pour un ou plusieurs champs de balise.
seo-description: Obtient toutes les valeurs du dictionnaire de balises définies pour un ou plusieurs champs de balise.
seo-title: getTagFieldValues
solution: Experience Manager
title: getTagFieldValues
topic: Scene7 Image Production System API
uuid: 92d84dfc-6a6c-4876-9670-1152adb6317c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getTagFieldValues{#gettagfieldvalues}

Obtient toutes les valeurs du dictionnaire de balises définies pour un ou plusieurs champs de balise.

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
| ` *`companyHandle`*` | `xsd:string` | Oui | poignée du contenant le champ de balise. |
| ` *`fieldHandleArray`*` | `types:HandleArray` | Oui | Un tableau de champs gère les valeurs de balise que vous souhaitez renvoyer. |

**Output (getTagFieldValuesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`fieldArray`*` | `types:TagFieldValuesArray` | Oui | Tableau des valeurs de balise dans le dictionnaire pour chaque champ demandé. |

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

