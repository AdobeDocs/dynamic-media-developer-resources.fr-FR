---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2e08a62b-9499-41f8-927b-89bed972b4eb
TQID: 'https://experienceleague.adobe.com/bcpeaqLRZ8ClN2OulOfO9ujXzz44Yb2HTmy-GyPQ8mU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fondu </span> </p> </td> 
   <td colname="col2"> <p> Spécifie le type d'effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. Utilisez <span class="codeph"> aucun </span> pour afficher et masquer instantanément ; <span class="codeph"> fondu </span> fournit un effet de fondu progressif (non pris en charge dans Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique le temps, en secondes, qui s’écoule entre le dernier événement souris/toucher enregistré par la barre de contrôle et le masquage de cette dernière. </p> <p> Si cette valeur est définie sur <span class="codeph"> -1 </span> le composant ne déclenche jamais son effet de masquage automatique et reste toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durée </span> </span> </p> </td> 
   <td colname="col2"> <p> Définit la durée de l’animation d’entrée et de sortie en fondu, en secondes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif. Cette commande est ignorée sur les appareils tactiles, où le masquage automatique de la barre de commande est désactivé.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]

