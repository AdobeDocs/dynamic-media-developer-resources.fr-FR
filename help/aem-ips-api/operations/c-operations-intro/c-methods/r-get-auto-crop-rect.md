---
description: Renvoie une zone recadrée pour une image en fonction de sa couleur d’arrière-plan ou de sa transparence.
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e291597a-b863-42dd-88dc-13398b734410
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 13%

---

# getAutoCropRect{#getautocroprect}

Renvoie une zone recadrée pour une image en fonction de sa couleur d’arrière-plan ou de sa transparence.

Syntaxe

## Types d’utilisateurs autorisés {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**Entrée (getAutoCropRectParam)**

>[!NOTE]
>
>Spécifiez autoColorCropOptions ou autoTransparentCropOptions lors de l’appel de cette méthode.

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestionnaire de l’entreprise avec la ressource que vous souhaitez utiliser. |
| assetHandle | `xsd:string` | Oui | Gestion de la ressource que vous souhaitez utiliser. |
| autoColorCropOptions | `types:AutoColorCropOptions` | Non | Calculez le rectangle de recadrage en fonction de la couleur. Voir [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| autoTransparentCropOptions | `types:AutoTransparentCropOptions` | Non | Calculez le rectangle de recadrage en fonction de la transparence. Voir [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**Sortie (getAutoCropRectReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| xOffset | `xsd:int` | Oui | Coordonnée en pixels de départ gauche de la région de recadrage calculée. |
| Décalage | `xsd:int` | Oui | Coordonnée du premier pixel de la région de recadrage calculée. |
| largeur | `xsd:int` | Oui | Largeur de la région de recadrage calculée (en pixels). |
| hauteur | `xsd:int` | Oui | Hauteur de la région de recadrage calculée (en pixels). |

## Exemples {#section-ba65bd66086d491cad1cea535954ee1f}

**Requête**

```java
<getAutoCropRectParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <companyHandle>c|3578</companyHandle>
  <assetHandle>a|3192146</assetHandle>
  <autoColorCropOptions>
    <corner>UpperLeft</corner>
    <tolerance>0.5</tolerance>
  </autoColorCropOptions>
</getAutoCropRectParam>
```

**Réponse**

```java
<getAutoCropRectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <xOffset>452</xOffset>
  <yOffset>66</yOffset>
  <width>1271</width>
  <height>1874</height>
</getAutoCropRectReturn>
```

>[!MORELIKETHIS]
>
>* [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)
