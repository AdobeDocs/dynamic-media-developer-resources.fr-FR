---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. </p> <p>Utilisez <span class="codeph"> none</span> pour afficher et masquer instantanément. Utilisez <span class="codeph"> fondu</span> pour obtenir un effet de fondu progressif et de fondu. </p> <p>Le fondu n’est pas pris en charge sur Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Indique la durée (en secondes) entre le dernier événement de souris/touche enregistré par la barre de contrôle et la barre de contrôle de l’heure masquée. </p> <p> S’il est défini sur <span class="codeph"> -1</span>, le composant ne déclenche jamais son effet de masquage automatique et reste toujours visible à l’écran. </p> </td> 
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
