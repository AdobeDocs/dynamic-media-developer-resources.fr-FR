---
description: Définit la cible de zoom associée à une image de ressource. Il remplace les cibles de zoom existantes.
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# setZoomTargets{#setzoomtargets}

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

**Input (setZoomTargetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Poignée de la société. |
| assetHandle | `xsd:string` | Oui | Ressource avec la cible de zoom à définir. |
| zoomTargetArray | `types:ZoomTargetDefinitionArray` | Oui | Tableau des définitions de cibles de zoom. |

**Sortie (setZoomTargetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| zoomTargetHandleArray | `types:HandleArray` | Oui | Ensemble de gestionnaires vers les cibles de zoom créées par cette opération. |

## Exemples {#section-a2f14c7a1499443e96d099ea8a76c182}

Cet exemple de code définit un tableau de cibles de zoom par nom, position (axe x et y), largeur, hauteur et affecte le tableau à une ressource. La réponse contient des poignées pour les cibles de zoom nouvellement créées.

**Requête**

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
