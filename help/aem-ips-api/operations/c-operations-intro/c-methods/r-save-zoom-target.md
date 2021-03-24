---
description: Créez ou modifiez une cible de zoom.
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 20%

---


# saveZoomTarget{#savezoomtarget}

Créez ou modifiez une cible de zoom.

Syntaxe

## Type d&#39;utilisateur autorisé {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-4a23983cae4e49a098e9bbe736933996}

**Entrée (saveZoomTargetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société avec la cible de zoom à enregistrer. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de la cible de zoom. |
| `*`zoomTargetHandle`*` | `xsd:string` | Non | Modifie ou crée une cible de zoom. |
| `*`name`*` | `xsd:string` | Oui | Nom de la cible de zoom. |
| `*`xPosition`*` | `xsd:int` | Oui | Emplacement du pixel à gauche. |
| `*`yPosition`*` | `xsd:int` | Oui | Emplacement du pixel supérieur. |
| `*`width`*` | `xsd:int` | Oui | Largeur de la cible de zoom. |
| `*`height`*` | `xsd:int` | Oui | Hauteur de la cible de zoom. |
| `*`Données utilisateur`*` | `xsd:string` | Oui | Pour obtenir des informations spécifiques au client. Peut contenir n’importe quel type de données. |

**Output (saveZoomTargetReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`zoomTargetHandle`*` | `xsd:string` | Oui | Gérer la nouvelle cible de zoom. |

## Exemples {#section-509c472c316549cdb228d7e1cfa8400a}

Cet exemple de code enregistre une cible de zoom. La réponse renvoie la poignée de cible de zoom.

**Request**

```java
<saveZoomTargetParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <name>My Zoom Target</name>
   <xPosition>2</xPosition>
   <yPosition>2</yPosition>
   <width>10</width>
   <height>10</height>
   <userData>My User Data</userData>
</saveZoomTargetParam>
```

**Réponse**

```java
<saveZoomTargetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <zoomTargetHandle>34194|9|301</zoomTargetHandle>
</saveZoomTargetReturn>
```

