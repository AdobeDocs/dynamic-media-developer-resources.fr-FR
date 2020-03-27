---
description: Image floue. Applique un filtre de flou aux données image.
seo-description: Image floue. Applique un filtre de flou aux données image.
seo-title: op_blur
solution: Experience Manager
title: op_blur
topic: Scene7 Image Serving - Image Rendering API
uuid: 8405bbb5-fe09-412e-9b52-0af2c01f48b9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_blur{#op-blur}

Image floue. Applique un filtre de flou aux données image.

`op_blur= *`radius`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Rayon du filtre de flou en pixels (réel 0.100). </p></td> 
 </tr> 
</table>

*`radius`* est exprimée en pixels par rapport à l’image composite. Également utilisé pour lisser les effets de calque.

## Propriétés {#section-92573fe2c07746a7bab93a81fc3d208d}

Calque, commande. S’applique au calque actif ou à l’image composite, le cas échéant `layer=comp`.

## Par défaut {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, sans effet de flou.

## Exemple {#section-1ebacde68388492eb108ae0fcd7424db}

Efface l’arrière-plan d’une image. Une image de masque distincte est référencée par `catalog::MaskPath`. Notez que vous `layer=0`devez spécifier explicitement, sinon `op_blur` vous appliquerez à l’ensemble de l’image composite.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
