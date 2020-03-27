---
description: Créez ou modifiez un  de zoom.
seo-description: Créez ou modifiez un  de zoom.
seo-title: saveZoomTarget
solution: Experience Manager
title: saveZoomTarget
topic: Scene7 Image Production System API
uuid: 197f7a2a-39ea-41cc-8e3a-76f9fe1b37d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveZoomTarget{#savezoomtarget}

Créez ou modifiez un  de zoom.

Syntaxe

## Type d’utilisateur autorisé {#section-823cd9f0557045bca51da66768b5ba74}

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
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée vers le avec le de zoom  que vous souhaitez enregistrer. |
| ` *`assetHandle`*` | `xsd:string` | Oui | Poignée du de zoom. |
| ` *`zoomTargetHandle`*` | `xsd:string` | Non | Modifie ou crée un de zoom. |
| ` *`nom`*` | `xsd:string` | Oui | Nom de l’ de zoom. |
| ` *`xPosition`*` | `xsd:int` | Oui | Emplacement du pixel gauche. |
| ` *`yPosition`*` | `xsd:int` | Oui | Emplacement du pixel supérieur. |
| ` *`width`*` | `xsd:int` | Oui | Zoom  la largeur du. |
| ` *`height`*` | `xsd:int` | Oui | Zoom  la hauteur. |
| ` *`Données utilisateur`*` | `xsd:string` | Oui | Pour obtenir des informations spécifiques au client. Peut contenir n’importe quel type de données. |

**Output (saveZoomTargetReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`zoomTargetHandle`*` | `xsd:string` | Oui | Traitement du nouveau de zoom. |

## Exemples {#section-509c472c316549cdb228d7e1cfa8400a}

Cet exemple de code enregistre un  de zoom. La réponse renvoie la poignée  zoom.

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

