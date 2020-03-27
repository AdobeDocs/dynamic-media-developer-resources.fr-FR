---
description: 'null'
seo-description: 'null'
seo-title: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
topic: Dynamic media
uuid: 12595a89-bad5-4224-aeff-52ce6bb615ee
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`durée`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositive|tourner|auto</span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet appliqué au changement d’image. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> la diapositive</span> active un  où l’ancienne image s’écoule hors de l’et où la nouvelle image s’imbrique dans l’ de l’. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> actionner</span> active un effet de retournement de page lorsqu’un utilisateur peut faire glisser l’un des quatre coins de la planche et effectuer un retournement de page interactif. </p> <p>Lors de l’utilisation de <span class="codeph"> ourner</span> , l’aspect du composant est contrôlé avec le modificateur <span class="codeph"> pageturnstyle</span> et la classe CSS <span class="codeph"> .s7pagedivider</span> est ignorée. </p> <p>Remarque :  <p><span class="codeph"> l’animation de tournage</span> n’est pas prise en charge sur Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> définit le du cadre de tournage sur les ordinateurs de bureau et le de diapositives sur les périphériques tactiles. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p>Indique la durée, en secondes, d’une <span class="codeph"> diapositive</span> ou d’un effet de  de tournage <span class="codeph"></span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-4d25a3f483834d2b9586fa70270ce6bd}

Facultatif.

## Par défaut {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## Exemple {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
