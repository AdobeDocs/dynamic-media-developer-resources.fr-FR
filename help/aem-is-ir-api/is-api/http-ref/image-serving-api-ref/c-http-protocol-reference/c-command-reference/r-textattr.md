---
title: Attr du texte
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

# Attr du texte{#textattr}

Attributs de calque de texte. Spécifie des attributs supplémentaires pour les calques de texte qui ne sont pas disponibles en tant que commandes rtf.

` textAttr= *`anticrénelage`*[, *`res`*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Res </span> </span> </p> </td> 
  <td class="stentry"> <p>Il permet de mettre à l’échelle le calque de texte sans modifier la taille des polices. Des valeurs de résolution plus élevées augmentent la taille du texte rendu par rapport à la taille de la zone de travail ; Des valeurs plus faibles réduisent la taille du texte. Résolution du texte en points par pouce (int supérieur à 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> le lissage des </span> ressources </span> </p> </td> 
  <td class="stentry"> <p>Contrôle le mode d’anticrénelage utilisé par le moteur de rendu de texte. </p> <p> <span class="codeph"> désactivé | Norme | Croustillant | pointu | Fort | lisse </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> de </span> </p> </td> 
      <td class="stentry"> <p>Désactiver le lissage du texte. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norme </span> </p> </td> 
      <td class="stentry"> <p>Activez le mode standard de lissage du texte (par défaut). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> croquant </span> </p> </td> 
      <td class="stentry"> <p>Sélectionnez Photoshop mode <span class="codeph"> anticrénelage net </span> ( <span class="codeph"> textPs= </span> only). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> tranchant </span> </p> </td> 
      <td class="stentry"> <p>Sélectionnez Photoshop mode <span class="codeph"> anticrénelage net </span> ( <span class="codeph"> textPs= </span> uniquement). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fort </span> </p> </td> 
      <td class="stentry"> <p>Sélectionnez Photoshop mode <span class="codeph"> anticrénelage strong </span> ( <span class="codeph"> textPs= </span> only). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Mode resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Contrôle la façon dont res est utilisé lors du rendu du texte </p> <p> <span class="codeph"> Rés fixes | AutoRes | Rés max. </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> Rés fixes </span> </p> </td> 
      <td class="stentry"> <p>Utilisez la résolution spécifiée. </p> <p>Utilisez cette action si le texte doit être rendu dans une taille exacte par rapport à la zone composite. Le texte peut être tronqué à la taille du calque (si spécifiée) si la zone de texte est trop petite. C’est la seule <span class="varname"> option resMode </span> prise en charge par <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> AutoRes </span> </p> </td> 
      <td class="stentry"> <p>Ajustez automatiquement la résolution pour remplir au mieux le calque rect avec le texte. </p> <p>Permet d’ajuster automatiquement la taille du texte afin que la zone de texte soit remplie autant que possible, sans risque de troncation. Si le retour automatique à la ligne est activé, le texte peut être réencapsulé à la résolution finale. La <span class="varname"> résolution </span> est ignorée si <span class="codeph"> autoRes </span> est sélectionné. Non pris en charge par <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> Rés max. </span> </p> </td> 
      <td class="stentry"> <p>Utilisez la résolution spécifiée ; Réduisez-la si nécessaire pour éviter que le texte ne soit tronqué au calque rect. </p> <p>Permet d’effectuer le rendu du texte à la résolution spécifiée, tant qu’aucun écrêtage ne se produit. S’il y a écrêtage, la résolution est automatiquement diminuée pour s’assurer que tout le texte est contenu entièrement à l’intérieur de la zone de texte. Si le retour automatique à la ligne est activé, le texte peut être réencapsulé à la résolution finale. Non pris en charge par <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Si la taille du calque de texte n’est pas spécifiée avec size= ou si seule la largeur est spécifiée, les paramètres 'autoRes' et 'maxRes' sont ignorés. Dans ce cas, la résolution spécifiée est utilisée pour le rendu du texte. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Renvoi à la ligne </span> du mot </span> </p> </td> 
  <td class="stentry"> <p>Spécifie le mode d’encapsulation. </p> <p> <span class="codeph"> Renvoi à la ligne | NoWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> NoWrap </span> </p> </td> 
      <td class="stentry"> <p>Désactiver le retour automatique à la ligne. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> envelopper </span> </p> </td> 
      <td class="stentry"> <p>Activez le retour automatique à la ligne standard. </p> <p>Il casse de longs mots, si nécessaire. <span class="codeph"> textPs= </span> prend uniquement en charge <span class="codeph"> l’habillage </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>Activer le retour automatique à la ligne insécable. </p> <p>Ne casse jamais un mot, même s’il est tronqué à la fin. Généralement utilisé avec <span class="codeph"> autoRes </span> ou <span class="codeph"> maxRes </span> pour s’assurer que les mots longs ne sont jamais cassés. </p> </td> 
     </tr> 
    </table> </p> <p>Les <span class="codeph"> deux renvoyer à la ligne </span> et <span class="codeph"> nbwrap </span> sont automatiquement renvoyés à la ligne sur les limites des mots et les traits d’union. </p> </td> 
 </tr> 
</table>

## Propriétés {#section-114ca0b8585b403c873e2251478ad1d5}

Attribut de calque de texte. Ignoré par les calques d’image, de couleur unie et d’effet. S’applique à `layer=0` si spécifié pour `layer=comp`.

## Par défaut {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Voir aussi {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
