---
description: Mise à l’échelle de l’image. Met à l’échelle une image par facteur par rapport à l’image en pleine résolution.
solution: Experience Manager
title: scale
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 89701a15-a0b6-460d-b0c1-5e25f3305380
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 4%

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
