---
description: Définit la cible de zoom associée à une image de fichier. Il remplace les cibles de zoom existantes.
seo-description: Définit la cible de zoom associée à une image de fichier. Il remplace les cibles de zoom existantes.
seo-title: setZoomTargets
solution: Experience Manager
title: setZoomTargets
topic: Scene7 Image Production System API
uuid: 5d0aecec-ebd8-4c69-9514-c29fae347ee6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 12%

---


# setZoomTargets{#setzoomtargets}

Définit la cible de zoom associée à une image de fichier. Il remplace les cibles de zoom existantes.

Syntaxe

## Types d&#39;utilisateur autorisés {#section-c5e1863e9cb1426591bfea513620b6ab}

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
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée de société. |
| ` *`assetHandle`*` | `xsd:string` | Oui | Ressource avec la cible de zoom que vous souhaitez définir. |
| ` *`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | Oui | Tableau des définitions de cible de zoom. |

**Output (setZoomTargetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`zoomTargetHandleArray`*` | `types:HandleArray` | Oui | Ensemble de poignées des cibles de zoom créées par cette opération. |

## Exemples {#section-a2f14c7a1499443e96d099ea8a76c182}

Cet exemple de code définit un tableau de cibles de zoom par nom, position (axes x et y), largeur, hauteur et affecte le tableau à une ressource. La réponse contient des poignées pour les nouvelles cibles de zoom.

**Request**

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

