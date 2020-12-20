---
description: 'null'
seo-description: 'null'
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: 30f133bd-09c7-4d70-bcc4-d961bb028e55
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 5%

---


# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade  </span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. Utilisez <span class="codeph"> none </span> pour afficher et masquer instantanément ; <span class="codeph"> fondu </span> fournit un effet de fondu progressif d’entrée et de sortie (non pris en charge sur Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide  </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique la durée, en secondes, entre le dernier événement souris/tactile que la barre de contrôle enregistre et la barre de contrôle temporelle masque. </p> <p> Si elle est définie sur <span class="codeph"> -1 </span>, le composant ne déclenche jamais son effet de masquage automatique et reste toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durée  </span> </span> </p> </td> 
   <td colname="col2"> <p> Définit la durée de l’animation en fondu et en fondu, en secondes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif. Cette commande est ignorée sur les périphériques tactiles, où la barre de contrôle est masquée automatiquement.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
