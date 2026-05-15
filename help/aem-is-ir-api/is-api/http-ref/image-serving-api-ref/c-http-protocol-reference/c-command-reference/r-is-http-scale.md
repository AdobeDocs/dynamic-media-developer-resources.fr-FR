---
title: mettre à l'échelle
description: Mise à l’échelle de l’image. Met à l’échelle une image source de calque par rapport à l’image en pleine résolution.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
TQID: 'https://experienceleague.adobe.com/qC-yBofpV9CNTTjb8Ll1EYV6Q1YA0BUsLLEHadfLAu8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 2%

---

# mettre à l&#39;échelle{#scale}

Mise à l’échelle de l’image. Met à l’échelle une image source de calque par rapport à l’image en pleine résolution.

`scale= *`factor`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p>facteur </span> <span class="varname"></p> </td> 
  <td class="stentry"> <p>Facteur d’échelle (réel, supérieur à 0,0). </p></td> 
 </tr> 
</table>

Aucune mise à l’échelle n’est appliquée lors de la `scale=1`. *`factor`* plus petite que 1,0 réduit et plus grande que 1,0 agrandit l’image source.

## Propriétés {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Attribut image/mask Source. Ignoré si `size=` est également spécifié pour le calque actif. Remplace `res=`. S’applique au calque 0 s’il est spécifié pour `layer=comp`. Ignoré si le calque n’est pas associé à une image ou un masque.

## Par défaut {#section-26e64904362342a5a62c5f6598f330c4}

S’il n’est pas spécifié, `res=` est utilisé. Si `res=` n’est pas spécifié, l’image est utilisée sans mise à l’échelle.

## Voir aussi {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
