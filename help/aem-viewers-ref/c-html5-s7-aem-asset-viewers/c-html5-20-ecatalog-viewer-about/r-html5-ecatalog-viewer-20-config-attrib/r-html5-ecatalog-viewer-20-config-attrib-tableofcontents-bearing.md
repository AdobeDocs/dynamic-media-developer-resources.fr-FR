---
title: TableOfContents.bearing
description: TableOfContents.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 2%

---

# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`Délai avant masquage automatique`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> ajusté-latéral|ajusté-vertical</span> </p> </td> 
   <td> <p> Contrôle la direction de l’aspect du panneau déroulant. </p> <p>Lorsqu’il est défini sur <span class="codeph"> ajuster verticalement</span>, le composant déplace d’abord la position du panneau de base vers le bas de son bouton et tente de déployer le panneau à droite ou à gauche à partir de l’emplacement de base. À chaque tentative, le composant vérifie si le panneau est clipsé par un conteneur extérieur. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement dans les directions droite et gauche. </p> <p>Lorsqu’il est défini sur <span class="codeph"> ajustement latéral</span>, le composant utilise une logique similaire, mais déplace d’abord la base vers la droite, en essayant de descendre et de monter les directions de déploiement. Ensuite, il déplace la base vers la gauche, en essayant de descendre et de monter les directions de déploiement. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> Délai avant masquage automatique</span></span> </p> </td> 
   <td> <p> Définit le délai en secondes pour le minuteur de masquage automatique déroulant qui masque le panneau lorsqu’un utilisateur est inactif. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-55436ddd78b04f538dbb9a7a8463feae}

Facultatif.

## Par défaut {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## Exemple {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
