---
title: ControlBar.transition
description: Attribut de configuration pour la visionneuse Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 950b1230-5c4b-4222-87e2-d069287fc3ff
TQID: 'https://experienceleague.adobe.com/mKDRX66X6uQLgPVw6jyc5VxKyKQlsM0DgQGSuGlHeBs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 119
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Attribut de configuration pour la visionneuse Video360.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aucun|fondu</span> </p> </td> 
   <td colname="col2"> <p> Spécifie le type d'effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. </p> <p>Utilisez <span class="codeph"> aucun</span> pour afficher et masquer instantanément. Utilisez <span class="codeph"> fondu</span> pour obtenir un effet d’entrée et de sortie en fondu progressif. </p> <p>La fondu n'est pas pris en charge dans Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Indique le temps, en secondes, qui s’écoule entre le dernier événement souris/toucher enregistré par la barre de contrôle et le masquage de cette dernière. </p> <p> Si la valeur <span class="codeph"> -1</span> le composant ne déclenche jamais son effet de masquage automatique et reste toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durée </span> </span> </p> </td> 
   <td colname="col2"> <p>Définit la durée de l’animation d’entrée et de sortie en fondu, en secondes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```
