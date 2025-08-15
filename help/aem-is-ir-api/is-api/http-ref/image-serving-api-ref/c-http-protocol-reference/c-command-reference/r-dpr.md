---
title: Collecte de données (RMR)
description: Rapport en pixels du périphérique (DPR)&mdash ; également connu sous le nom de CSS pixel ratio&mdash ; est la relation entre les pixels physiques et les pixels logiques d’un périphérique.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d64ca9ed-7d8e-4a13-9c9d-acb7de3e31ed
source-git-commit: 63c0e3b494b6d583117dad01643946900855802e
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 2%

---

# Collecte de données (RMR){#dpr}

Le rapport de pixels de périphérique (DPR), également connu sous le nom de rapport de pixels CSS, est la relation entre les pixels physiques d’un périphérique et les pixels logiques. Surtout avec l’avènement des écrans Retina, la résolution en pixels des appareils mobiles modernes augmente à un rythme rapide.

L’activation de l’optimisation du rapport de pixels de l’appareil rend l’image à la résolution native de l’écran, ce qui la rend nette.

Actuellement, la densité en pixels de l’affichage provient des valeurs d’en-tête CDN d’Akamai.

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> de </span> </span> </p> </td> 
  <td class="stentry"> <p>Désactivez l’optimisation DPR au niveau d’une URL d’image individuelle. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> on, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>Remplacez la valeur DPR détectée par Smart Imaging par une valeur personnalisée (telle que détectée par une logique côté client ou d’autres moyens). La valeur autorisée pour dprValue est tout nombre supérieur à 0. </p> </td> 
 </tr> 
</table>


Vous pouvez utiliser `dpr=on,dprValue` même si le paramètre DPR au niveau de l’entreprise est désactivé.

En raison de l’optimisation DPR, lorsque l’image résultante est supérieure au paramètre MaxPix Dynamic Media, la largeur MaxPix est toujours reconnue en conservant le format de l’image.

| Taille d’image demandée | Valeur DPR | Taille de l’image délivrée |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2 448 x 1 500 |
| 816 x 500 | 4 | 3264 x 2000 |

Les valeurs DPR sont basées sur les valeurs côté client détectées du CDN combiné. Ces valeurs sont parfois inexactes. Par exemple, iPhone5 avec `dpr=2`, et iPhone12 avec dpr=3, les deux affichent `dpr=2`. Néanmoins, pour les appareils haute résolution, l’envoi est préférable à l’envoi `dpr=2` `dpr=1`de fichiers . La meilleure façon de surmonter cette inexactitude, cependant, est d’utiliser DPR côté client pour vous donner des valeurs précises à 100 %. Et cela fonctionne pour n’importe quel appareil, qu’il s’agisse d’Apple ou de tout autre appareil qui a été lancé. Voir [Utilisation de l’imagerie dynamique avec le rapport](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en) de pixels du périphérique côté client.

## Propriétés

Un attribut de requête. Il n’a aucun effet si `dpr` est désactivé ou si `dprValue=1`.

## Par défaut

`dpr=off`


## Exemple

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Voir aussi

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [réseau](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [imagerie dynamique](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)
