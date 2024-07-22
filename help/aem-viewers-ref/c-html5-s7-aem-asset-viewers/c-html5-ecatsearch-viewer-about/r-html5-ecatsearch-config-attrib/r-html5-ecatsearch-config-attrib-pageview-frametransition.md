---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 19239fa8-65a8-487f-9370-42bb93d862d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`duration`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositive|tour|auto</span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet appliqué au changement d’image. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> slide</span> active une transition où l’ancienne image s’éloigne de la vue et la nouvelle image s’étend vers la vue. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> tourner </span> active un effet de saut de page lorsqu’un utilisateur peut faire glisser l’un des quatre coins de la page et effectuer un saut de page interactif. </p> <p>Lors de l’utilisation de <span class="codeph"> ourner</span>, l’aspect du composant est contrôlé à l’aide du modificateur <span class="codeph"> pageturnstyle</span> et la classe CSS <span class="codeph"> .s7pagedivider</span> est ignorée. </p> <p>Remarque :  <p>L’animation <span class="codeph"> tour</span> n’est pas prise en charge sur Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> définit la transition d’image de rotation sur les systèmes de bureau et la transition de diapositive sur les appareils tactiles. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p>Indique la durée en secondes d’un effet de transition <span class="codeph"> slide</span> ou <span class="codeph"> tours</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-4d25a3f483834d2b9586fa70270ce6bd}

Facultatif.

## Par défaut {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## Exemple {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
