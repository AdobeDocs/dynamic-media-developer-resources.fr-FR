---
title: SpinView.transition
description: SpinView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: fcffe282-65a5-4093-8838-71a64085b387
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`time`*[, *`easing`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fois</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le temps en secondes nécessaire à l’animation d’une seule action de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> assouplissement</span></span> </p> </td> 
   <td colname="col2"> <p> Crée une illusion d'accélération ou de décélération qui rend la transition plus naturelle. Vous pouvez définir l'assouplissement sur l'une des options suivantes : </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 (auto) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 (linéaire) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (quadratique) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (cube) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (quartique) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (quintic) </li> 
     </ul> </p> <p>Le mode automatique utilise toujours une transition linéaire lorsque le zoom élastique est désactivé (par défaut). Sinon, elle s'adapte à l'une des autres fonctions d'assouplissement en fonction du temps de transition. En d'autres termes, plus le temps de transition est court, plus la fonction d'assouplissement est utilisée pour accélérer l'effet d'accélération ou de décélération. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
