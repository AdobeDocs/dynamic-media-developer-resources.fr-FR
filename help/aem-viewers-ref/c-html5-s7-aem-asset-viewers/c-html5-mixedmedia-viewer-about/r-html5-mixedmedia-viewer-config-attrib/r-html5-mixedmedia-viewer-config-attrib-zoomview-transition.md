---
description: ZoomView.transition
solution: Experience Manager
title: ZoomView.transition
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,User
exl-id: bb00a1c9-aa6f-428f-8d57-241ee1efa082
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *``*[, *`temporisation`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> heure</span></span> </p> </td> 
   <td colname="col2"> <p> Indique la durée en secondes de l’animation d’une seule action d’étape de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> assouplissement</span></span> </p> </td> 
   <td colname="col2"> <p> Crée une illusion d'accélération ou de décélération qui rend la transition plus naturelle. Vous pouvez définir l’assouplissement sur l’une des options suivantes : </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (auto) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (linéaire) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (quadratique) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cubique) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (quartique) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quintique) </li> 
     </ul> </p> <p>Le mode automatique utilise toujours une transition linéaire lorsque le zoom élastique est désactivé (par défaut). Sinon, il convient à l’une des autres fonctions d’assouplissement en fonction du temps de transition. En d’autres termes, plus le temps de transition est court, plus la fonction d’assouplissement est utilisée pour accélérer l’effet d’accélération ou de décélération. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
