---
description: Créez ou modifiez une cible de zoom.
solution: Experience Manager
title: Enregistrer la cible de zoom
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 19%

---

# Enregistrer la cible de zoom{#savezoomtarget}

Créez ou modifiez une cible de zoom.

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
| CompanyHandle | `xsd:string` | Oui | Poignée de l’entreprise avec la cible de zoom que vous souhaitez enregistrer. |
| AssetHandle | `xsd:string` | Oui | Poignée de la cible de zoom. |
| Poignée de cibles de zoom | `xsd:string` | Non | Modifie ou crée une cible de zoom. |
| nom | `xsd:string` | Oui | Nom de la cible de zoom. |
| xPosition | `xsd:int` | Oui | Emplacement du pixel gauche. |
| yPosition | `xsd:int` | Oui | Emplacement du pixel supérieur. |
| largeur | `xsd:int` | Oui | Largeur de la cible de zoom. |
| hauteur | `xsd:int` | Oui | Hauteur de cible de zoom. |
| Données utilisateur | `xsd:string` | Oui | Pour des informations spécifiques au client. Peut contenir n’importe quel type de données. |

**Output (saveZoomTargetReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Poignée de cibles de zoom | `xsd:string` | Oui | Poignée de la cible de zoom nouvellement créée. |

## Exemples {#section-509c472c316549cdb228d7e1cfa8400a}

Cet exemple de code enregistre une cible de zoom. La réponse renvoie la poignée de cible de zoom.

**Demander**

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
