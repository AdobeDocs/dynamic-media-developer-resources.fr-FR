---
description: 'null'
seo-description: 'null'
seo-title: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
topic: Dynamic media
uuid: e60603a5-06dc-43e3-a380-b4d97fc539f1
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 8%

---


# PageView.maxloadradius{#pageview-maxloadradius}

[!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Indique le comportement de préchargement du composant. </p> <p>Lorsqu’il est défini sur <span class="codeph"> -1</span>, le composant précharge toutes les images du catalogue en cas d’inactivité. </p> <p> Lorsqu'il est défini sur <span class="codeph"> 0</span>, le composant charge uniquement l'image actuellement visible, l'image précédente et l'image suivante. </p> <p>Définissez <span class="codeph"><span class="varname"> preloadnbr</span></span> pour définir le nombre de cadres invisibles autour du cadre actuellement affiché qui sont préchargés en état d’inactivité. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-4b7952997f9240e581d21bcdb173f9af}

Facultatif.

## Par défaut {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Exemple {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
