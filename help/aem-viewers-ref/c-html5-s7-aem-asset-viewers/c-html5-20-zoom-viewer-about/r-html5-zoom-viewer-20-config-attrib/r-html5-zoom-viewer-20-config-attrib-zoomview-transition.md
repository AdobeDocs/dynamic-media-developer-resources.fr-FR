---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.
solution: Experience Manager
title: ZoomView.
topic: Dynamic media
uuid: 1d58d230-f056-4cd8-a36f-b0f5d43483a3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *``*[, *`temporisation`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> heure</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le temps en secondes que l’animation d’une seule action d’étape de zoom prend. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> assouplissement</span></span> </p> </td> 
   <td colname="col2"> <p> Crée une illusion d’accélération ou de décélération qui rend le plus naturel. Vous pouvez définir l’accélération sur l’une des options suivantes : </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (auto) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (linéaire) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (quadratique) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cubique) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (quartique) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quintique) </li> 
     </ul> </p> <p>Le mode Auto utilise toujours des  linéaires lorsque le zoom élastique est désactivé (valeur par défaut). Sinon, il s’adapte à l’une des autres fonctions d’assouplissement en fonction de l’heure  du. Autrement dit, plus le temps de  est court, plus la fonction d'assouplissement est utilisée pour accélérer l'effet d'accélération ou de décélération. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`0.5,0`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`transition=2,2`
