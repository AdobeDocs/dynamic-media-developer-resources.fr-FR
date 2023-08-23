---
title: dpr
description: Device Pixel Ratio (DPR)&mdash;également appelé CSS pixel ratio&mdash;est la relation entre les pixels physiques et les pixels logiques d’un appareil.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 21d6aed6baee24922732461fe680f6cc93bd0d06
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 2%

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

Les valeurs DPR sont basées sur les valeurs côté client détectées du réseau de diffusion de contenu groupé. Ces valeurs sont parfois inexactes. Par exemple, iPhone5 avec `dpr=2`, et iPhone12 avec dpr=3, les deux affichent `dpr=2`. Toujours pour les appareils haute résolution, l’envoi `dpr=2` est préférable à l’envoi `dpr=1`. La meilleure façon de surmonter cette inexactitude consiste toutefois à utiliser le RPD côté client pour vous donner des valeurs entièrement précises. Et ça marche pour n&#39;importe quel appareil, qu&#39;il s&#39;agisse d&#39;Apple ou de tout autre appareil qui a été lancé. Voir [Utilisation de l’imagerie dynamique avec rapport des pixels côté client](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## Propriétés



## Par défaut

`dpr=off`


## Exemple

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Voir aussi

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [network](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [Imagerie dynamique](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)