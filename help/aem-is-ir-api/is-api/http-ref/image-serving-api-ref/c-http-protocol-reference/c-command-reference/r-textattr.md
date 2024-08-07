---
title: textAttr
description: Attributs de calque de texte. Spécifie des attributs supplémentaires pour les calques de texte qui ne sont pas disponibles en tant que commandes rtf.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# textAttr{#textattr}

Attributs de calque de texte. Spécifie des attributs supplémentaires pour les calques de texte qui ne sont pas disponibles en tant que commandes rtf.

` textAttr= *`res`*[, *`antiAliasing`*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span> </span> </p> </td> 
  <td class="stentry"> <p>Il permet de mettre le calque de texte à l’échelle sans modifier la taille des polices. Des valeurs de résolution plus élevées augmentent la taille du texte rendu par rapport à la taille de la zone de travail ; des valeurs plus petites réduisent la taille du texte. Résolution du texte en points par pouce (int supérieur à 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> anti-alias </span> </span> </p> </td> 
  <td class="stentry"> <p>Contrôle le mode anti-crénelage utilisé par le moteur de rendu de texte. </p> <p> <span class="codeph"> désactivé | standard | crisper | sharp | fort | smog </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> off </span> </p> </td> 
      <td class="stentry"> <p>Désactivez l’anti-crénelage du texte. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> standard </span> </p> </td> 
      <td class="stentry"> <p>Activez le mode anti-alias de texte standard (par défaut). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> crisp </span> </p> </td> 
      <td class="stentry"> <p>Sélectionnez le mode anti-alias Photoshop <span class="codeph"> crisp </span> ( <span class="codeph"> textPs= </span> uniquement). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> sharp </span> </p> </td> 
      <td class="stentry"> <p>Sélectionnez le mode anti-alias Photoshop <span class="codeph"> sharp </span> ( <span class="codeph"> textPs= </span> uniquement). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> strong </span> </p> </td> 
      <td class="stentry"> <p>Sélectionnez le mode anti-alias Photoshop <span class="codeph"> strong </span> ( <span class="codeph"> textPs= </span> uniquement). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Contrôle l’utilisation des termes lors du rendu du texte </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>Utilisez la résolution spécifiée. </p> <p>Utilisez cette option si le texte doit être rendu avec une taille exacte par rapport à la zone de travail composite. Le texte peut être tronqué à la taille du calque (le cas échéant) si la zone de texte est trop petite. Il s'agit de la seule option <span class="varname"> resMode </span> prise en charge par <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>Ajustez automatiquement la résolution pour remplir au mieux le recto du calque avec le texte. </p> <p>Utilisez pour ajuster automatiquement la taille du texte afin que la zone de texte soit remplie autant que possible, sans risque de troncature. Si le retour automatique à la ligne est activé, le texte peut être réencapsulé à la résolution finale. <span class="varname"> res </span> est ignoré si <span class="codeph"> autoRes </span> est sélectionné. Non pris en charge par <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>Utilisez la résolution spécifiée ; réduisez-la si nécessaire afin d’empêcher que le texte ne soit tronqué dans la recette du calque. </p> <p>Utilisez pour effectuer le rendu du texte à la résolution spécifiée, à condition qu’aucun détourage ne se produise. En cas de détourage, la résolution est automatiquement réduite afin de garantir que tout le texte est contenu entièrement dans la zone de texte. Si le retour automatique à la ligne est activé, le texte peut être réencapsulé à la résolution finale. Non pris en charge par <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Si la taille du calque de texte n’est pas spécifiée avec size= ou si seule la largeur est spécifiée, les paramètres "autoRes" et "maxRes" sont ignorés. Dans ce cas, la résolution spécifiée est utilisée pour le rendu du texte. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap </span> </span> </p> </td> 
  <td class="stentry"> <p>Indique le mode d’encapsulation. </p> <p> <span class="codeph"> wrap | noWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>Désactivez le retour automatique à la ligne. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> wrap </span> </p> </td> 
      <td class="stentry"> <p>Activez le retour automatique à la ligne standard. </p> <p>Cela casse les mots longs, si nécessaire. <span class="codeph"> textPs= </span> ne prend en charge que <span class="codeph"> wrap </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>Activez le retour automatique à la ligne incessant. </p> <p>Ne casse jamais un mot, même s'il est tronqué à la fin. Généralement utilisé avec <span class="codeph"> autoRes </span> ou <span class="codeph"> maxRes </span> pour s’assurer que les mots longs ne sont jamais rompus. </p> </td> 
     </tr> 
    </table> </p> <p><span class="codeph"> encapsule </span> et <span class="codeph"> font encapsuler automatiquement </span> sur les limites de mots et les tirets. </p> </td> 
 </tr> 
</table>

## Propriétés {#section-114ca0b8585b403c873e2251478ad1d5}

Attribut de calque de texte. Ignoré par les calques d’image, de couleur unie et d’effet. S’applique à `layer=0` s’il est spécifié pour `layer=comp`.

## Par défaut {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Voir aussi {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
