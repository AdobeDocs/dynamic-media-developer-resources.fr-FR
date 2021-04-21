---
description: Attributs de calque de texte. Spécifie des attributs supplémentaires pour les calques de texte qui ne sont pas disponibles en tant que commandes rtf.
solution: Experience Manager
title: textAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 1%

---


# textAttr{#textattr}

Attributs de calque de texte. Spécifie des attributs supplémentaires pour les calques de texte qui ne sont pas disponibles en tant que commandes rtf.

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res  </span> </span> </p> </td> 
  <td class="stentry"> <p>Permet de mettre à l’échelle le calque de texte sans modifier les tailles de police. Des valeurs de résolution plus élevées augmentent la taille du texte rendu par rapport à la taille de la zone de travail ; des valeurs plus petites réduisent la taille du texte. Résolution du texte en points par pouce (int supérieur à 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing  </span> </span> </p> </td> 
  <td class="stentry"> <p>Contrôle le mode de lissage utilisé par le moteur de rendu de texte. </p> <p> <span class="codeph"> off | norme | croustillant | sharp | fort | lisse  </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> désactivé </span> </p> </td> 
      <td class="stentry"> <p>Désactivez l’anti-aliasing de texte. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norme  </span> </p> </td> 
      <td class="stentry"> <p>Activez le mode standard de lissage du texte (par défaut). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> croustillant  </span> </p> </td> 
      <td class="stentry"> <p>Sélectionnez le mode de lissage Photoshop <span class="codeph"> croustillant </span> ( <span class="codeph"> textPs= </span> uniquement). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> net  </span> </p> </td> 
      <td class="stentry"> <p>Sélectionnez le mode de lissage Photoshop <span class="codeph"> sharp </span> ( <span class="codeph"> textPs= </span> uniquement). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> Renforcée </span> </p> </td> 
      <td class="stentry"> <p>Sélectionnez le mode de lissage Photoshop <span class="codeph"> strong </span> ( <span class="codeph"> textPs= </span> uniquement). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Contrôle l’utilisation de res lors du rendu du texte. </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes  </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes  </span> </p> </td> 
      <td class="stentry"> <p>Utilisez la résolution spécifiée. </p> <p>Utilisez cette option si le texte doit être rendu dans une taille exacte par rapport à la trame de composition. Le texte peut être coupé à la taille du calque (s’il est spécifié) si la zone de texte est trop petite. Il s'agit de la seule option <span class="varname"> resMode </span> prise en charge par <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes  </span> </p> </td> 
      <td class="stentry"> <p>Ajustez automatiquement la résolution afin de remplir au mieux le calque rect avec le texte. </p> <p>Permet d’ajuster automatiquement la taille du texte afin que la zone de texte soit remplie autant que possible, sans risque de troncature. Si le renvoi à la ligne est activé, le texte peut être réencapsulé à la résolution finale. <span class="varname"> res  </span> est ignoré si  <span class="codeph"> autoRes  </span> est sélectionné. Non pris en charge par <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes  </span> </p> </td> 
      <td class="stentry"> <p>utiliser la résolution spécifiée ; réduisez-la si nécessaire afin d’éviter que le texte ne soit tronqué au rect de calque. </p> <p>Utilisez cette option pour effectuer le rendu du texte à la résolution exacte spécifiée, à condition qu’il n’y ait pas d’écrêtage. En cas d’écrêtage, la résolution est automatiquement diminuée pour s’assurer que tout le texte est contenu entièrement à l’intérieur de la zone de texte. Si le renvoi à la ligne est activé, le texte peut être réencapsulé à la résolution finale. Non pris en charge par <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Si la taille du calque de texte n’est pas spécifiée avec size= ou si seule la largeur est spécifiée, les paramètres autoRes et maxRes sont ignorés et la résolution spécifiée est utilisée pour le rendu du texte. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap  </span> </span> </p> </td> 
  <td class="stentry"> <p>Indique le mode d’encapsulation. </p> <p> <span class="codeph"> envelopper | noWrap | nbWrap  </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap  </span> </p> </td> 
      <td class="stentry"> <p>Désactivez l’encapsulation des mots. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> inclusion </span> </p> </td> 
      <td class="stentry"> <p>Activez le renvoi à la ligne standard. </p> <p>Rompt les mots longs si nécessaire. <span class="codeph"> textPs=  </span> ne prend en charge que le  <span class="codeph"> renvoi  </span>à la ligne. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap  </span> </p> </td> 
      <td class="stentry"> <p>Activez le renvoi à la ligne sans fin. </p> <p>Ne casse jamais un mot, même s'il est tronqué à la fin. Habituellement utilisé conjointement avec <span class="codeph"> autoRes </span> ou <span class="codeph"> maxRes </span> pour s’assurer que les mots longs ne sont jamais rompus. </p> </td> 
     </tr> 
    </table> </p> <p><span class="codeph"> renvoie à la fois </span> et <span class="codeph"> nbwrap </span> auto-encapsulé sur les limites de mots et les traits d’union. </p> </td> 
 </tr> 
</table>

## Propriétés {#section-114ca0b8585b403c873e2251478ad1d5}

Attribut de calque de texte. Ignoré par les calques d’image, de couleur unie et d’effet. S&#39;applique à `layer=0` si spécifié pour `layer=comp`.

## Par défaut {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Voir aussi {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
