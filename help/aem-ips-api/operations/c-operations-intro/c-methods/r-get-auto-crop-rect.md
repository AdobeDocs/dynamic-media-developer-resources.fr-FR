---
description: Renvoie une zone recadrée pour une image en fonction de sa couleur ou de sa transparence d’arrière-plan.
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e291597a-b863-42dd-88dc-13398b734410
TQID: 'https://experienceleague.adobe.com/cDQ-P-vZGfOyPASRMfemIKnphk5GavTU85m4vJq83bc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 152
ht-degree: 13%

---

# getAutoCropRect{#getautocroprect}

Renvoie une zone recadrée pour une image en fonction de sa couleur ou de sa transparence d’arrière-plan.

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

**Input (getAutoCropRectParam)**

>[!NOTE]
>
>Spécifiez autoColorCropOptions ou autoTransparentCropOptions lors de l’appel de cette méthode.

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Poignée de la société contenant la ressource que vous souhaitez utiliser. |
| assetHandle | `xsd:string` | Oui | Poignée de la ressource que vous souhaitez utiliser. |
| autoColorCropOptions | `types:AutoColorCropOptions` | Non | Calculez le rectangle de recadrage en fonction de la couleur. Voir [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| autoTransparentCropOptions | `types:AutoTransparentCropOptions` | Non | Calculer le rectangle de recadrage en fonction de la transparence. Voir [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**Output (getAutoCropRectReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| xOffset | `xsd:int` | Oui | Coordonnée des pixels gauche de départ de la zone de recadrage calculée. |
| Décalage | `xsd:int` | Oui | Coordonnée du pixel supérieur de départ de la zone de recadrage calculée. |
| largeur | `xsd:int` | Oui | Largeur de la zone de recadrage calculée (en pixels). |
| hauteur | `xsd:int` | Oui | Hauteur de la zone de recadrage calculée (en pixels). |

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
