---
title: ControlBar.transition
description: ControlBar.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`durée`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. </p> <p>Utilisation <span class="codeph"> none</span> pour un spectacle et un masquage instantanés. Utilisation <span class="codeph"> fade</span> afin de créer un effet de fondu progressif et de fondu. </p> <p>Le fondu n’est pas pris en charge sur Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Indique la durée (en secondes) entre le dernier événement de souris/touche enregistré par la barre de contrôle et la durée (en secondes) pendant laquelle la barre de contrôle est masquée. </p> <p> Si la variable est définie sur <span class="codeph"> -1</span>, le composant ne déclenche jamais son effet de masquage automatique et reste toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durée</span> </span> </p> </td> 
   <td colname="col2"> <p>Définit la durée de l’animation de fondu et de fondu, en secondes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
