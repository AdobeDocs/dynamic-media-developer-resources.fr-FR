---
title: dpr
description: Le rapport pixel d’appareil (DPR)&mdash;également appelé rapport pixel CSS&mdash;est la relation entre les pixels physiques et les pixels logiques d’un appareil.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d64ca9ed-7d8e-4a13-9c9d-acb7de3e31ed
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 2%

---

# dpr{#dpr}

Le rapport pixel d’appareil (DPR), également appelé rapport pixel CSS, est la relation entre les pixels physiques et les pixels logiques d’un appareil. Surtout avec l’avènement des écrans Retina, la résolution en pixels des appareils mobiles modernes augmente à un rythme rapide.

Activer l’optimisation du rapport pixel d’appareil rend l’image à la résolution native de l’écran, ce qui la rend nette.

Actuellement, la densité en pixels de l’affichage provient des valeurs d’en-tête Akamai CDN.

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sur </span> </span> </p> </td> 
  <td class="stentry"> <p>Désactivez l’optimisation du DPR au niveau de l’URL d’une image individuelle. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> le, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>Remplacez la valeur DPR détectée par l’imagerie dynamique par une valeur personnalisée (telle que détectée par une logique côté client ou par d’autres moyens). La valeur autorisée pour dprValue est n’importe quel nombre supérieur à 0. </p> </td> 
 </tr> 
</table>


Vous pouvez utiliser `dpr=on,dprValue` même si le paramètre DPR au niveau de la société est désactivé.

En raison de l’optimisation du DPR, lorsque l’image créée est supérieure au paramètre MaxPix Dynamic Media, la largeur MaxPix est toujours reconnue en conservant les proportions de l’image.

| Taille d’image demandée | Valeur DPR | Taille de l’image diffusée |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1 632 x 1 000 |
| 816 x 500 | 3 | 2 448 x 1 500 |
| 816 x 500 | 4 | 3264 x 2000 |

Les valeurs DPR sont basées sur les valeurs côté client détectées du réseau CDN groupé. Ces valeurs sont parfois inexactes. Par exemple, iPhone5 avec `dpr=2` et iPhone12 avec dpr=3 affichent tous deux `dpr=2`. Néanmoins, pour les appareils à haute résolution, envoyer des `dpr=2` est préférable à envoyer des `dpr=1`. La meilleure façon de surmonter cette inexactitude consiste toutefois à utiliser le DPR côté client pour vous donner des valeurs parfaitement précises. Et cela fonctionne pour n’importe quel appareil, qu’il s’agisse d’Apple ou de tout autre appareil existant. Voir [Utilisation de l’imagerie dynamique avec le rapport pixel d’appareil côté client](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=fr).

## Propriétés

Attribut de requête. Cela n’a aucun effet si `dpr` est désactivé ou `dprValue=1`.

## Par défaut

`dpr=off`


## Exemple

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Voir aussi

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [network](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [imagerie dynamique](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=fr)
