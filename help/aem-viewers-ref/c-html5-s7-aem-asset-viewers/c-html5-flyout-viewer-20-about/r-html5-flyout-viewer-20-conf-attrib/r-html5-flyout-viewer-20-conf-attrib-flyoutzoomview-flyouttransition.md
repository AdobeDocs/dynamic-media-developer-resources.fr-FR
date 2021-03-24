---
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
feature: Dynamic Media Classic, Visionneuses, SDK/API, Fenêtre déroulante
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|fade  </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet appliqué lorsque la vue de la fenêtre déroulante est affichée ou masquée. Avec <span class="codeph"> none </span>, l'image de fenêtre déroulante s'affiche instantanément lorsqu'elle est activée et prête ; <span class="codeph"> la diapositive </span> fait jouer l'animation de la diapositive de gauche à droite ; <span class="codeph"> fondu </span> applique une transition alpha à l'image de la fenêtre déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> démonstration  </span> </span> </p> </td> 
   <td colname="col2"> <p> Nombre de secondes que l'animation d'affichage prend pour se terminer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay  </span> </span> </p> </td> 
   <td colname="col2"> <p> Délai en secondes entre l'action de l'utilisateur qui initie l'animation d'affichage et le début de l'animation d'affichage lui-même. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetime  </span> </span> </p> </td> 
   <td colname="col2"> <p> Nombre de secondes pendant lesquelles l'animation de masquage se termine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay  </span> </span> </p> </td> 
   <td colname="col2"> <p> Délai en secondes entre l'action de l'utilisateur qui initie l'animation de masquage et le début de l'animation de masquage elle-même. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
