---
description: Définit la cible de zoom associée à une image de ressource. Il remplace les cibles de zoom existantes.
solution: Experience Manager
title: Définir les cibles de zoom
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# Définir les cibles de zoom{#setzoomtargets}

Définit la cible de zoom associée à une image de ressource. Il remplace les cibles de zoom existantes.

Syntaxe

## Types d’utilisateurs autorisés {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-161f8c733cc4439f94a06e12119d4226}

**Entrée (setZoomTargetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Pseudo de l’entreprise. |
| AssetHandle | `xsd:string` | Oui | Ressource avec la cible de zoom que vous souhaitez définir. |
| Tableau de cibles zoom | `types:ZoomTargetDefinitionArray` | Oui | Tableau des définitions de cibles de zoom. |

**Output (setZoomTargetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| zoomTargetHandleArray | `types:HandleArray` | Oui | Ensemble des poignées des cibles de zoom créées par cette opération. |

## Exemples {#section-a2f14c7a1499443e96d099ea8a76c182}

Cet exemple de code définit une matrice de cibles de zoom par nom, position (axes x et y), largeur, hauteur et affecte la matrice à une ressource. La réponse contient des indicateurs aux cibles de zoom nouvellement créées.

**Demander**

```java
<setZoomTargetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <zoomTargetArray>
      <items>
         <name>zoomTarget2</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
      <items>
         <name>zoomTarget3</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
   </zoomTargetArray>
</setZoomTargetsParam>
```

**Réponse**

```java
<setZoomTargetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zoomTargetHandleArray>
      <items>a|947|9|41</items>
      <items>a|948|9|42</items>
   </zoomTargetHandleArray>
</setZoomTargetsReturn>
```
