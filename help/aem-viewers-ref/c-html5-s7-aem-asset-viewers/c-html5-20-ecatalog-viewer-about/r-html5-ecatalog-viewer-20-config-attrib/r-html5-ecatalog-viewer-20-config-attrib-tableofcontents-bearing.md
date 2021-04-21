---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 2%

---


# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> ajusté latéral|ajusté-vertical</span> </p> </td> 
   <td> <p> Contrôle l’orientation de l’aspect du panneau déroulant. </p> <p>Lorsqu'il est défini sur <span class="codeph"> ajustement vertical</span>, le composant déplace d'abord la position du panneau de base vers le bas de son bouton et tente de déployer le panneau soit vers la droite soit vers la gauche depuis l'emplacement de base. A chaque tentative, le composant vérifie si le panneau est coupé par un conteneur extérieur. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement dans les directions droite et gauche. </p> <p>Lorsqu'il est défini sur <span class="codeph"> raccord-latéral</span>, le composant utilise une logique similaire, mais déplace d'abord la base vers la droite, en essayant d'effectuer des déploiements vers le bas et vers le haut. Ensuite, il déplace la base vers la gauche, en essayant de déployer des directions vers le bas et vers le haut. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Définit le délai en secondes du minuteur de masquage automatique de la liste déroulante qui masque le panneau lorsqu’un utilisateur est inactif. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-55436ddd78b04f538dbb9a7a8463feae}

Facultatif.

## Par défaut {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## Exemple {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
