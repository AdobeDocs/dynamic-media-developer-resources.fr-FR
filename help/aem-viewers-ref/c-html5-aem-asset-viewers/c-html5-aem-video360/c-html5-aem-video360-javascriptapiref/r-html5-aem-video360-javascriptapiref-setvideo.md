---
description: Référence de l’API JavaScript pour le lecteur vidéo360
solution: Experience Manager
title: setVideo
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo 360 VR
role: Développeur, Professionnel
exl-id: e1894d96-6f37-4e34-a709-5b0121bd0696
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 4%

---

# setVideo{#setvideo}

Référence de l’API JavaScript pour le lecteur vidéo360

`setVideo(videoUrl)`

Définit la nouvelle vidéo externe. Peut être appelé à tout moment, avant et après `init()`. Si elle est appelée après `init()`, le lecteur permute la vidéo au moment de l’exécution.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Paramètres {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl  </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Chaîne</span>} : URL absolue vers la nouvelle vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Viewers/space_station_360")
```
