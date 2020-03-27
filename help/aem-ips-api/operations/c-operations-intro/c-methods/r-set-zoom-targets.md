---
description: Définit le de zoom associé à une image de fichier. Il remplace les  de zoom existantes.
seo-description: Définit le de zoom associé à une image de fichier. Il remplace les  de zoom existantes.
seo-title: setZoomTargets
solution: Experience Manager
title: setZoomTargets
topic: Scene7 Image Production System API
uuid: 5d0aecec-ebd8-4c69-9514-c29fae347ee6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setZoomTargets{#setzoomtargets}

Définit le de zoom associé à une image de fichier. Il remplace les  de zoom existantes.

Syntaxe

## Types d’utilisateur autorisés {#section-c5e1863e9cb1426591bfea513620b6ab}

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
| ` *`companyHandle`*` | `xsd:string` | Oui |  poignée. |
| ` *`assetHandle`*` | `xsd:string` | Oui | Ressource avec le de zoom que vous souhaitez définir. |
| ` *`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | Oui | Tableau de définitions de  de zoom. |

**Output (setZoomTargetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`zoomTargetHandleArray`*` | `types:HandleArray` | Oui | Ensemble de poignées du de zoom créé par cette opération. |

## Exemples {#section-a2f14c7a1499443e96d099ea8a76c182}

Cet exemple de code définit un tableau de de zoom par nom, position (axes x et y), largeur, hauteur et affecte le tableau à un fichier. La réponse contient des poignées au nouveau de zoom.

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

