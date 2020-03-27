---
description: 'null'
seo-description: 'null'
seo-title: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
topic: Dynamic media
uuid: c8d63ad9-6867-4b90-a113-6a75e394f706
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.iconEffect{#pageview-iconeffect}

[!DNL `[PageView.|<containerId>_pageView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`]

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Permet à l’effet <span class="codeph"></span> d’icône de s’afficher en haut de l’image lorsque celle-ci est à l’état Réinitialisé et suggère une action disponible pour interagir avec l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> nombre</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le nombre maximal de fois où l’ <span class="codeph"> iconeffect</span> apparaît et réapparaît. La valeur <span class="codeph"> -1</span> indique que l’icône réapparaît toujours indéfiniment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fondre</span></span> </p> </td> 
   <td colname="col2"> <p>Indique la durée de l’animation d’affichage ou de masquage, en secondes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Définit le nombre de secondes pendant lesquelles l’effet <span class="codeph"></span> iconographique reste entièrement visible avant d’être masqué automatiquement. C’est-à-dire le moment qui suit la fin de l’animation en fondu mais avant le  d’animation en fondu. Un paramètre de <span class="codeph"> 0</span> désactive le comportement de masquage automatique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-b6e5e52698d4492f9d6350e7e312bb1b}

Facultatif.

## Par défaut {#section-7d0fc8fa09b34c288ed32ef7faa84604}

[!DNL `1,1,0.3,3`]

## Exemple {#section-95db1bfcccf241089654363203b19977}

[!DNL `iconeffect=0`]
