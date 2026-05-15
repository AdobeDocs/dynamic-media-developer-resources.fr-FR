---
title: textAttr
description: Attributs de calque de texte. Spécifie des attributs supplémentaires pour les calques de texte qui ne sont pas disponibles en tant que commandes RTF.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
TQID: 'https://experienceleague.adobe.com/7md74Pcl5SuFEi6v8mdpYTAxj3bJZTykMzg7bpT8Aqo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 458
ht-degree: 0%

---

# textAttr{#textattr}

Attributs de calque de texte. Spécifie des attributs supplémentaires pour les calques de texte qui ne sont pas disponibles en tant que commandes RTF.

` textAttr= *`res`*[, *`antiAliasing`*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span> </span> </p> </td> 
  <td class="stentry"> <p>Il permet de mettre à l’échelle le calque de texte sans modifier la taille de la police. Des valeurs de résolution plus élevées augmentent la taille du texte rendu par rapport à la taille de la zone de travail ; des valeurs plus petites réduisent la taille du texte. Résolution du texte en points par pouce (nombre entier supérieur à 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing </span> </span> </p> </td> 
  <td class="stentry"> <p>Contrôle le mode anti-crénelage utilisé par le moteur de rendu de texte. </p> <p> <span class="codeph"> off | norme | croustillant | net | solide | lisse </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> de </span> </p> </td> 
      <td class="stentry"> <p>Désactivez le lissage du texte. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> </span> de norme <span class="codeph"> </p> </td> 
      <td class="stentry"> <p>Activez le mode de lissage de texte standard (par défaut). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> croustillant </span> </p> </td> 
      <td class="stentry"> <p>Sélectionnez le mode de lissage de Photoshop <span class="codeph"> une </span> nette ( <span class="codeph"> textPs= </span> uniquement). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> pointue </span> </p> </td> 
      <td class="stentry"> <p>Sélectionnez le mode anti-crénelage de Photoshop <span class="codeph"> une </span> nette ( <span class="codeph"> textPs= </span> uniquement). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> forte </span> </p> </td> 
      <td class="stentry"> <p>Sélectionnez le mode de lissage de Photoshop <span class="codeph"> des </span> forts ( <span class="codeph"> textPs= </span> uniquement). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Contrôle l’utilisation de la suite lors du rendu du texte </p> <p> <span class="codeph"> FixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> </span> FixedRes <span class="codeph"> </p> </td> 
      <td class="stentry"> <p>Utiliser la résolution spécifiée. </p> <p>Utilisez si le texte doit être rendu dans une taille exacte par rapport à la zone de travail composite. Le texte peut être tronqué à la taille du calque (si elle est spécifiée) si la zone de texte est trop petite. Il s’agit de la seule option de </span> resMode <span class="varname"> prise en charge par <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>Ajustez automatiquement la résolution pour remplir au mieux le calque droit avec le texte. </p> <p>Permet d’ajuster automatiquement la taille du texte afin que la zone de texte soit remplie autant que possible, sans risque de troncature. Si le retour à la ligne est activé, le texte peut être réencapsulé à la résolution finale. Le </span> <span class="varname"> res est ignoré si <span class="codeph"> autoRes </span> est sélectionné. Non pris en charge par <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>Utilisez la résolution spécifiée, diminuez-la si nécessaire pour empêcher que le texte ne soit tronqué au calque droit. </p> <p>Permet d’effectuer le rendu du texte à la résolution spécifiée, tant qu’aucun écrêtage ne se produit. En cas d’écrêtage, la résolution est automatiquement réduite pour s’assurer que tout le texte est contenu dans la zone de texte. Si le retour à la ligne est activé, le texte peut être réencapsulé à la résolution finale. Non pris en charge par <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Si la taille du calque de texte n'est pas spécifiée avec size= ou si seule la largeur est spécifiée, les paramètres 'autoRes' et 'maxRes' sont ignorés. Dans ce cas, la résolution spécifiée est utilisée pour effectuer le rendu du texte. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap </span> </span> </p> </td> 
  <td class="stentry"> <p>Indique le mode d’encapsulation. </p> <p> <span class="codeph"> wrap | noWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>Désactivez l’habillage des mots. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> wrap </span> </p> </td> 
      <td class="stentry"> <p>Activez le renvoi à la ligne standard. </p> <p>Il casse de longs mots, si nécessaire. <span class="codeph"> textPs= </span> ne prend en charge que les </span> de retour à la ligne <span class="codeph">. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>Activez le retour à la ligne sans rupture. </p> <p>Ne casse jamais un mot, même s'il est tronqué à la fin. Généralement utilisé avec <span class="codeph"> autoRes </span> ou <span class="codeph"> maxRes </span> pour s'assurer que les mots longs ne sont jamais rompus. </p> </td> 
     </tr> 
    </table> </p> <p>Les options <span class="codeph"> et <span class="codeph"> sont </span> et </span> automatiquement sur les limites des mots et les tirets. </p> </td> 
 </tr> 
</table>

## Propriétés {#section-114ca0b8585b403c873e2251478ad1d5}

Attribut de calque de texte. Ignoré par les calques d’image, de couleur unie et d’effet. S’applique à `layer=0` si spécifié pour `layer=comp`.

## Par défaut {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Voir aussi {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
