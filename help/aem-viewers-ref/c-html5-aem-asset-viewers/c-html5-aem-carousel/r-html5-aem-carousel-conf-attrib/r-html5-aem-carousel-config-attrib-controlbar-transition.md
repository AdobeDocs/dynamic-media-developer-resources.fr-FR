---
title: ControlBar.transition
description: Attribut de configuration pour la visionneuse de carrousel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
TQID: 'https://experienceleague.adobe.com/oVi-FxRdW7mQ-HlLoExaCG6cAB56WDuupA2RnEM7pqY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Attribut de configuration pour la visionneuse de carrousel.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aucun|fondu</span> </p> </td> 
   <td colname="col2"> <p> Spécifie le type d'effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. </p> <p>Définissez-le sur <span class="codeph"> aucun</span> par exemple pour afficher/masquer instantanément. </p> <p>Définissez cette option sur <span class="codeph"> fondu</span> afin de fournir un effet de fondu d’entrée/sortie progressif. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le temps, en secondes, qui s’écoule entre le dernier événement souris/toucher enregistré par la barre de contrôle et le masquage de cette dernière. </p> <p>Si cette valeur est définie sur <span class="codeph"> -1</span> le composant ne déclenche jamais son effet de masquage automatique et reste donc toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p> Définit la durée de l’animation d’entrée/sortie en fondu en secondes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif. Cette commande est ignorée sur les appareils tactiles où le masquage automatique de la barre de commande est désactivé.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
