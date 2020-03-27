---
description: 'null'
seo-description: 'null'
seo-title: SpinView.
solution: Experience Manager
title: SpinView.
topic: Dynamic media
uuid: d5cc319a-fb0b-41d3-a118-f00376a127e4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`temporisation`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> heure</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le temps en secondes que l’animation d’une seule action d’étape de zoom prend. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> assouplissement</span></span> </p> </td> 
   <td colname="col2"> <p> Crée une illusion d’accélération ou de décélération qui rend le plus naturel. Vous pouvez définir l’accélération sur l’une des options suivantes : </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 (auto) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 (linéaire) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (quadratique) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (cubique) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (quartique) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (quintique) </li> 
     </ul> </p> <p>Le mode Auto utilise toujours des  linéaires lorsque le zoom élastique est désactivé (valeur par défaut). Sinon, il s’adapte à l’une des autres fonctions d’assouplissement en fonction de l’heure  du. Autrement dit, plus le temps de  est court, plus la fonction d'assouplissement est utilisée pour accélérer l'effet d'accélération ou de décélération. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
