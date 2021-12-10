---
title: PageView.frametransition
description: PageView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026c2fc5-0460-481c-aca9-ddd25371779c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 5%

---

# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`durée`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositive|changement|auto</span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet appliqué au changement d’image. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> diapositive</span> active une transition dans laquelle l’ancien cadre défile de l’affichage et le nouveau cadre se glisse dans l’affichage. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> ourner</span> active un effet de saut de page lorsqu’un utilisateur peut faire glisser l’un des quatre coins de la page et effectuer un saut de page interactif. </p> <p>When <span class="codeph"> ourner</span> est utilisé. L’aspect du composant est contrôlé à l’aide de la fonction <span class="codeph"> pageturnstyle</span> et le <span class="codeph"> .s7pagedivider</span> La classe CSS est ignorée. </p> <p>Remarque :  <p><span class="codeph"> ourner</span> L’animation n’est pas prise en charge sur Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> définit la transition d’image de rotation sur les systèmes de bureau et la transition de diapositive sur les périphériques tactiles. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p>Indique la durée en secondes d’un événement <span class="codeph"> diapositive</span> ou <span class="codeph"> ourner</span> effet de transition. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-4d25a3f483834d2b9586fa70270ce6bd}

Facultatif.

## Par défaut {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## Exemple {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
