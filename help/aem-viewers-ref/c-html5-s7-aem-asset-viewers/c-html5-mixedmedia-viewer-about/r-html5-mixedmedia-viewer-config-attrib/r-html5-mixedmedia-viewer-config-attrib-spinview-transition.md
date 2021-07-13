---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,User
exl-id: fcffe282-65a5-4093-8838-71a64085b387
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`temporisation`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> heure</span></span> </p> </td> 
   <td colname="col2"> <p> Indique la durée en secondes de l’animation d’une seule action d’étape de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> assouplissement</span></span> </p> </td> 
   <td colname="col2"> <p> Crée une illusion d'accélération ou de décélération qui rend la transition plus naturelle. Vous pouvez définir l’assouplissement sur l’une des options suivantes : </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 (auto) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 (linéaire) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (quadratique) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (cubique) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (quartique) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (quintique) </li> 
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
