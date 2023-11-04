---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2e08a62b-9499-41f8-927b-89bed972b4eb
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`durée`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade </span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. Utilisation <span class="codeph"> none </span> pour un affichage et un masquage instantanés; <span class="codeph"> fade </span> offre un effet de fondu progressif dans et de fondu (non pris en charge dans Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique la durée (en secondes) entre le dernier événement de souris/touche enregistré par la barre de contrôle et la barre de contrôle de l’heure masquée. </p> <p> Si la variable est définie sur <span class="codeph"> -1 </span> le composant ne déclenche jamais son effet de masquage automatique et reste toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durée </span> </span> </p> </td> 
   <td colname="col2"> <p> Définit la durée en secondes de l’animation de fondu et de fondu. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif. Cette commande est ignorée sur les périphériques tactiles, où la barre de contrôle est masquée automatiquement.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
