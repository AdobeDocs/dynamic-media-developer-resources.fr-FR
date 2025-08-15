---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d8b88ea2-38fe-41b8-89cb-c3603c513142
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---

# TableOfContents.bearing{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-latéral|fit-vertical</span> </p> </td> 
   <td> <p> Contrôle la direction de l’aspect du panneau déroulant. </p> <p>Lorsqu’il est défini sur <span class="codeph"> vertical</span> le composant déplace d’abord la position du panneau de base vers le bas de son bouton et tente de déployer le panneau vers la droite ou la gauche à partir de l’emplacement de base. À chaque tentative, le composant vérifie si le panneau est tronqué par un conteneur externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement dans les directions droite et gauche. </p> <p>Lorsqu'il est défini sur <span class="codeph"> ajusté-latéral</span> le composant utilise une logique similaire, mais déplace d'abord la base vers la droite, en essayant de descendre et de remonter les directions de déploiement. Ensuite, il déplace la base vers la gauche, essayant vers le bas et vers le haut les directions de déploiement. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Définit le délai en secondes pour le minuteur de masquage automatique de la liste déroulante qui masque le panneau lorsqu’un utilisateur est inactif. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-55436ddd78b04f538dbb9a7a8463feae}

Facultatif.

## Par défaut {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## Exemple {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
