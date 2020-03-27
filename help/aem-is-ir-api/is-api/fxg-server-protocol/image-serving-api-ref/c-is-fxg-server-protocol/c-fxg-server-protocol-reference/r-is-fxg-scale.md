---
description: Mise à l’échelle de l’image. Met à l’échelle une image par facteur par rapport à l’image en pleine résolution.
seo-description: Mise à l’échelle de l’image. Met à l’échelle une image par facteur par rapport à l’image en pleine résolution.
seo-title: scale
solution: Experience Manager
title: scale
topic: Scene7 Image Serving - Image Rendering API
uuid: db5bab94-e5c1-41fe-ab1b-5c62b6a798d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scale{#scale}

Mise à l’échelle de l’image. Met à l’échelle une image par facteur par rapport à l’image en pleine résolution.

`scale= *`facteur`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> facteur</span></span> </p> </td> 
  <td class="stentry"> <p>Facteur d’échelle (réel, &gt;0). </p></td> 
 </tr> 
</table>

## Par défaut {#section-e9e53959b35844579f0f1d7721b71f8e}

Si elle n’est pas spécifiée, l’image est utilisée sans mise à l’échelle.

## Exemple {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
