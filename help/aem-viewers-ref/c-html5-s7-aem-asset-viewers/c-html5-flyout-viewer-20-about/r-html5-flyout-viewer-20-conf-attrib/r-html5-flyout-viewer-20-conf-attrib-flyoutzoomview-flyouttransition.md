---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
topic: Dynamic media
uuid: f1a9f2bc-9a13-4980-9241-e835a0aadd2c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> aucun|diapositive|fondu </span></span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet appliqué lorsque le de fenêtre déroulante est affiché ou masqué. Avec <span class="codeph"> none </span>, l’image de la fenêtre déroulante s’affiche instantanément lorsqu’elle est activée et prête ; La <span class="codeph"> diapositive </span> fait lire l’animation de la diapositive de gauche à droite ; Le <span class="codeph"> fondu </span> applique un alpha à l’image de la fenêtre déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> démonstration </span></span> </p> </td> 
   <td colname="col2"> <p> Nombre de secondes nécessaires à l’achèvement de l’animation d’affichage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span></span> </p> </td> 
   <td colname="col2"> <p> Délai, en secondes, entre l’action de l’utilisateur qui initie l’animation d’affichage et le début de l’animation d’affichage elle-même. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hivernage </span></span> </p> </td> 
   <td colname="col2"> <p> Nombre de secondes nécessaires à l’achèvement de l’animation de masquage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay </span></span> </p> </td> 
   <td colname="col2"> <p> Délai en secondes entre l’action de l’utilisateur qui initie l’animation de masquage et le début de l’animation de masquage elle-même. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
