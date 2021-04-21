---
description: Image floue. Applique un filtre de flou aux données image.
solution: Experience Manager
title: op_blur
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

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

*`radius`* est exprimée en pixels par rapport à l’image composite. Également utilisé pour créer des effets de contour progressif sur les calques.

## Propriétés {#section-92573fe2c07746a7bab93a81fc3d208d}

Calque, commande. S’applique au calque actif ou à l’image composite si `layer=comp`.

## Par défaut {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, sans effet de flou.

## Exemple {#section-1ebacde68388492eb108ae0fcd7424db}

Efface l’arrière-plan d’une image. Une image de masque distincte est référencée par `catalog::MaskPath`. Notez que `layer=0`doit être spécifié explicitement, sinon `op_blur` sera appliqué à l&#39;image composite entière.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
