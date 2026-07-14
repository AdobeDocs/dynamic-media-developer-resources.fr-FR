---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 19239fa8-65a8-487f-9370-42bb93d862d5
TQID: 'https://experienceleague.adobe.com/X3qkuLchMxlcb-CpwM4-KLGNphsJe-DJMD3fsYz7KyY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 3%

---

# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`durée`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositive|tourner|auto</span> </p> </td> 
   <td colname="col2"> <p> Spécifie le type d'effet appliqué lors d'un changement d'image. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> diapositive</span> active une transition où l'ancien cadre ne s'affiche pas et le nouveau cadre s'affiche. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> tour</span> active un effet de basculement de page, lorsqu’un utilisateur peut faire glisser l’un des quatre coins de la planche et effectuer un basculement de page interactif. </p> <p>Lorsque <span class="codeph"> tour</span> est utilisé, l’aspect du composant est contrôlé avec le modificateur pageturnstyle</span> <span class="codeph"> et la classe CSS .s7pagedialog</span> <span class="codeph"> est ignorée. </p> <p>Remarque :  <p><span class="codeph"> tour</span> l'animation n'est pas prise en charge sur Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> définit la transition de l’angle de rotation sur les ordinateurs de bureau et la transition de glissement sur les appareils tactiles. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p>Spécifie la durée en secondes d'un effet de transition <span class="codeph"> diapositive</span> ou <span class="codeph"> tour</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-4d25a3f483834d2b9586fa70270ce6bd}

Facultatif.

## Par défaut {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## Exemple {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]

