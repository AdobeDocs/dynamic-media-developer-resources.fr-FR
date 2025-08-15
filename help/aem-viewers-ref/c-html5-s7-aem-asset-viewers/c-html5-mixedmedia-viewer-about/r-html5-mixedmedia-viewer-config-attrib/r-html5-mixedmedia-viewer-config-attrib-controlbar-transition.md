---
title: ControlBar.transition
description: ControlBar.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`Durée de masquage du`*[, *`délai`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Aucun|fondu</span> </p> </td> 
   <td colname="col2"> <p> Spécifie le type d’effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. </p> <p>N’utilisez <span class="codeph"> aucun pour l’affichage</span> instantané et le masquage. Utilisez <span class="codeph"> le fondu</span> pour obtenir un effet de fondu entrant et sortant progressif. </p> <p>Le fondu n’est pas pris en charge par Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Délai de masquage</span> </span> </p> </td> 
   <td colname="col2"> <p>Spécifie le temps en secondes entre le dernier événement souris/tactile enregistré par la barre de contrôle et le temps masqué par la barre de contrôle. </p> <p> S’il est défini sur <span class="codeph"> -1</span>, le composant ne déclenche jamais son effet de masquage automatique et reste toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> durée</span> </span> </p> </td> 
   <td colname="col2"> <p>Définit la durée en secondes de l’animation de fondu entrant et sortant. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
