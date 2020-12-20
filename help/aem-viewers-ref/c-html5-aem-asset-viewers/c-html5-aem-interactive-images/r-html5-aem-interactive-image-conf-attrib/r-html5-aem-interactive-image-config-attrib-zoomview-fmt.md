---
description: Indique le format d’image utilisé par le composant pour le chargement des images à partir du serveur Image Server.
seo-description: Indique le format d’image utilisé par le composant pour le chargement des images à partir du serveur Image Server.
seo-title: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
topic: Dynamic media
uuid: 73a2196f-0ece-497a-9a12-376dafbbae56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---


# ZoomView.fmt{#zoomview-fmt}

Indique le format d’image utilisé par le composant pour le chargement des images à partir du serveur Image Server.

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Si le format spécifié se termine par <span class="codeph"> -alpha</span>, le composant effectue le rendu des images sous forme de contenu transparent. Pour tous les autres formats d’image, le composant traite les images comme opaques. Par défaut, le composant possède un arrière-plan blanc. Par conséquent, pour le rendre transparent, définissez la propriété CSS <span class="codeph"> Background-color</span> sur <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
