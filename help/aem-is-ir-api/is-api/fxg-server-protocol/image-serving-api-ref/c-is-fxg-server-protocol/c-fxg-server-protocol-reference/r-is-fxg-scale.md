---
description: Mise à l’échelle de l’image. Met à l’échelle une image par facteur par rapport à l’image en pleine résolution.
solution: Experience Manager
title: mettre à l'échelle
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 89701a15-a0b6-460d-b0c1-5e25f3305380
TQID: 'https://experienceleague.adobe.com/MDIhDdn2fZiZgZMlEpdEZOwH0dAot4WGBGw2UcHij1I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 45
ht-degree: 4%

---

# mettre à l&#39;échelle{#scale}

Mise à l’échelle de l’image. Met à l’échelle une image par facteur par rapport à l’image en pleine résolution.

`scale= *`factor`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> facteur <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>Facteur d'échelle (réel, &gt;0). </p></td> 
 </tr> 
</table>

## Par défaut {#section-e9e53959b35844579f0f1d7721b71f8e}

Si elle n’est pas spécifiée, l’image est utilisée sans mise à l’échelle.

## Exemple {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
