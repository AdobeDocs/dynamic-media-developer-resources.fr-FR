---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 5%

---


# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`durée`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositive|tourner|auto</span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet appliqué au changement d’image. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> La </span> diapo désactive une transition où l’ancienne image s’égale de la vue et où la nouvelle image s’adapte à la vue. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> Le </span> changement de page active un effet de retournement de page lorsqu’un utilisateur peut faire glisser l’un des quatre coins de planche et effectuer un retournement de page interactif. </p> <p>Lorsque <span class="codeph"> tour</span> est utilisé, l'aspect du composant est contrôlé avec le modificateur <span class="codeph"> pageturnstyle</span> et la classe CSS <span class="codeph"> .s7pagedivider</span> est ignorée. </p> <p>Remarque :  <p><span class="codeph"> Le </span> tourniquet n'est pas pris en charge sur Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> </span> autodéfinit la transition d'image tournante sur les ordinateurs de bureau et la transition de diapositive sur les périphériques tactiles. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p>Spécifie la durée, en secondes, d'un effet de transition <span class="codeph"> slide</span> ou <span class="codeph"> tour</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-4d25a3f483834d2b9586fa70270ce6bd}

Facultatif.

## Par défaut {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## Exemple {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
