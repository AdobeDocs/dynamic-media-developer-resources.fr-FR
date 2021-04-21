---
description: Mise à l’échelle de l’image. Met à l’échelle une image source de calque par facteur par rapport à l’image à résolution complète.
solution: Experience Manager
title: scale
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 9%

---


# scale{#scale}

Mise à l’échelle de l’image. Met à l’échelle une image source de calque par facteur par rapport à l’image à résolution complète.

`scale= *`facteur`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> facteur</span> </p> </td> 
  <td class="stentry"> <p>Facteur d’échelle (réel, supérieur à 0,0). </p></td> 
 </tr> 
</table>

Aucune mise à l’échelle n’est appliquée lorsque `scale=1`. *`factor`* plus petite que 1,0 réduit la taille et plus grande que 1,0 agrandit l’image source.

## Propriétés {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Attribut image/masque source. Ignoré si `size=` est également spécifié pour le calque actif. Remplace `res=`. S’applique au calque 0 s’il est spécifié pour `layer=comp`. Ignoré si le calque n’est associé à aucune image ou masque.

## Par défaut {#section-26e64904362342a5a62c5f6598f330c4}

Si elle n&#39;est pas spécifiée, `res=` est utilisé. Si `res=` n’est pas spécifié, l’image est utilisée sans mise à l’échelle.

## Voir aussi {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) ,  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
