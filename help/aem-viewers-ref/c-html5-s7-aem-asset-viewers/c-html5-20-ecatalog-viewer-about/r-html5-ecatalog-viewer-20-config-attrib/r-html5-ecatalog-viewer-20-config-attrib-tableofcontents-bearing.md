---
title: TableOfContents.porting
description: TableOfContents.porting
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
TQID: 'https://experienceleague.adobe.com/i8oPW8fpqvU8JaUaJ-95swaFjD6YTHcqv21s3i7-L2g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 1%

---

# TableOfContents.porting{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-latéral|fit-vertical</span> </p> </td> 
   <td> <p> Contrôle la direction de l’aspect du panneau déroulant. </p> <p>Lorsqu’il est défini sur <span class="codeph"> vertical</span> le composant déplace d’abord la position du panneau de base vers le bas de son bouton et tente de déployer le panneau vers la droite ou la gauche à partir de l’emplacement de base. À chaque tentative, le composant vérifie si le panneau est tronqué par un conteneur externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement dans les directions droite et gauche. </p> <p>Lorsqu’il est défini sur <span class="codeph"> d’ajustement latéral</span> le composant utilise une logique similaire, mais déplace d’abord la base vers la droite, en essayant de descendre et de monter les directions de déploiement. Ensuite, il déplace la base vers la gauche, en essayant vers le bas et vers le haut les directions de déploiement. </p> </td> 
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

`fit-vertical,2`

## Exemple {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
