---
title: InteractiveSwatches.fmt
description: Attribut Configuration pour la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9a751b91-aeff-4ee1-b2fe-9bec416884ab
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# InteractiveSwatches.fmt{#interactiveswatches-fmt}

Attribut Configuration pour la visionneuse de vidéos interactives.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Spécifie le format d’image utilisé par le composant pour charger les images à partir d’Image Server. </p> <p>Si le format spécifié se termine par "<span class="codeph"> -alpha</span> », le composant effectue le rendu des images en tant que contenu transparent. Pour tous les autres formats d’image, le composant traite les images comme opaques. Le composant possède un arrière-plan blanc par défaut. Par conséquent, pour la rendre transparente, définissez la propriété CSS de couleur <span class="codeph"> d’arrière-plan</span> sur <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```
