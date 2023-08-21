---
title: dpr
description: Device Pixel Ratio (DPR)&mdash;également appelé CSS pixel ratio&mdash;est la relation entre les pixels physiques et les pixels logiques d’un appareil.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---

# dpr{#dpr}

Le ratio de pixels d’appareil (DPR), également appelé ratio de pixels CSS, est la relation entre les pixels physiques et les pixels logiques d’un appareil. Surtout avec l’avènement des écrans rétine, la résolution en pixels des appareils mobiles modernes augmente à un rythme rapide.

L’activation de l’optimisation du rapport de pixels de l’appareil rend l’image à la résolution native de l’écran, ce qui la rend nette.

Actuellement, la densité en pixels de l’affichage provient des valeurs d’en-tête Akamai CDN.

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> off </span> </span> </p> </td> 
  <td class="stentry"> <p>Désactivez l’optimisation du RGPD au niveau de l’URL d’une image individuelle. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> on, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>Remplacez la valeur RPD détectée par l’imagerie dynamique par une valeur personnalisée (comme détectée par une logique côté client ou par d’autres moyens). La valeur autorisée pour dprValue est tout nombre supérieur à 0. </p> </td> 
 </tr> 
</table>


Vous pouvez utiliser `dpr=on,dprValue` même si le paramètre RGPD au niveau de l’entreprise est désactivé.

En raison de l’optimisation du RPD, lorsque l’image créée est supérieure au paramètre MaxPix Dynamic Media , la largeur MaxPix est toujours reconnue en conservant les proportions de l’image.

| Taille d’image demandée | Valeur DPR | Taille de l’image diffusée |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1 632 x 1 000 |
| 816 x 500 | 3 | 2 448 x 1 500 |
| 816 x 500 | 4 | 3 264 x 2 000 |

## Propriétés



## Par défaut

`dpr=off`


## Exemple

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Voir aussi

[network](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [Imagerie dynamique](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)