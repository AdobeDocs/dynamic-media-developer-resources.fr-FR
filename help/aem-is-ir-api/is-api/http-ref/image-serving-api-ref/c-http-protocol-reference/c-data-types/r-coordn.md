---
title: coordN
description: Coordonnées normalisées. Permet de spécifier des positions relatives dans une image, telles que des décalages d’image ou des paramètres de recadrage, normalisés à la taille de l’image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
TQID: 'https://experienceleague.adobe.com/-dtYByOGK-mNAWc0yQBs4nu5sO1r-Ormq70iwdDZBjg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 0%

---

# coordN{#coordn}

Coordonnées normalisées. Permet de spécifier des positions relatives dans une image, telles que des décalages d’image ou des paramètres de recadrage, normalisés à la taille de l’image.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>décalage des coordonnées normalisé à la taille d’une image (réel, réel) </p></td> 
 </tr> 
</table>

Les valeurs positives se déplacent vers le bas à droite.

Souvent, la position de référence est le centre de l’image. Dans ce cas, `0,0` correspond au centre de l’image, `-0.5,-0.5` au coin supérieur gauche et `0.5,0.5` au coin inférieur droit.

Il est également utilisé pour spécifier la taille de l&#39;image ou la taille du rectangle par rapport à la taille du calque 0. Dans ce cas, la valeur doit être supérieure à 0. 0 peut indiquer qu’une valeur par défaut spécifique doit être utilisée. Une valeur `1,1` spécifie une taille égale à celle du calque 0.
