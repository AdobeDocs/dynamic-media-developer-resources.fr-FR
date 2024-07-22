---
title: op_blur
description: Image floue. Applique un filtre de flou aux données image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# op_blur{#op-blur}

Image floue. Applique un filtre de flou aux données image.

`op_blur= *`radius`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Rayon du filtre de flou en pixels (réel 0..100). </p></td> 
 </tr> 
</table>

*`radius`* est en pixels par rapport à l’image composite. Également utilisé pour ajouter des effets de calque.

## Propriétés {#section-92573fe2c07746a7bab93a81fc3d208d}

Couche, commande. S’applique au calque actif ou à l’image composite si `layer=comp`.

## Par défaut {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, sans effet de flou.

## Exemple {#section-1ebacde68388492eb108ae0fcd7424db}

Fusionner l’arrière-plan d’une image. Une image de masque distincte est référencée par `catalog::MaskPath`. Notez que `layer=0`doit être spécifié explicitement, sinon `op_blur` serait appliqué à l’ensemble de l’image composite.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
