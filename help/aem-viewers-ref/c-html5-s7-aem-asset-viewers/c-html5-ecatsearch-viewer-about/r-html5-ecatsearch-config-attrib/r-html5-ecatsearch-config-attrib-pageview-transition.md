---
description: 'null'
seo-description: 'null'
seo-title: PageView.
solution: Experience Manager
title: PageView.
topic: Dynamic media
uuid: c85ad85f-a802-4f5d-9046-00171ad2d9ca
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.{#pageview-transition}

[!DNL `[PageView.|<containerId>_pageView.]transition= *``*[, *`temporisation`*]`]

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> heure</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le temps en secondes que l’animation d’une seule action d’étape de zoom prend. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> assouplissement</span></span> </p> </td> 
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

## Propriétés {#section-ebfd9162c8504666bf0e4485bf3b1383}

Facultatif.

## Par défaut {#section-9f91ce6567384ab691e4d4f8a7015455}

[!DNL `0.5,0`]

## Exemple {#section-cb6b8793ee9946b8bf1cfddab8612db5}

[!DNL `transition=2,2`]
