---
description: Définit la cible de zoom associée à une image de ressource. Il remplace les cibles de zoom existantes.
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
TQID: 'https://experienceleague.adobe.com/JQfWp3-Xm1rGlAmd1qisxzo2irZy3aedScXmeBbL1Pk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 121
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
| companyHandle | `xsd:string` | Oui | Identifiant de la société. |
| assetHandle | `xsd:string` | Oui | Ressource avec la cible de zoom à définir. |
| zoomTargetArray | `types:ZoomTargetDefinitionArray` | Oui | Tableau de définitions de cibles de zoom. |

**Output (setZoomTargetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| zoomTargetHandleArray | `types:HandleArray` | Oui | Ensemble de poignées des cibles de zoom créées par cette opération. |

## Exemples {#section-a2f14c7a1499443e96d099ea8a76c182}

Cet exemple de code définit un tableau de cibles de zoom par nom, position (axes x et y), largeur, hauteur et affecte le tableau à une ressource. La réponse contient des poignées pour les cibles de zoom nouvellement créées.

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

