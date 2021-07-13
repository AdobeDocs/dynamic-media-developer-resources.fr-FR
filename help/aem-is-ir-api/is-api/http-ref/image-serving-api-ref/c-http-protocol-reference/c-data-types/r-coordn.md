---
description: Coordonnées normalisées. Utilisé pour spécifier des positions relatives dans une image, telles que des décalages d’image ou des paramètres de recadrage, normalisées selon la taille de l’image.
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# coordN{#coordn}

Coordonnées normalisées. Utilisé pour spécifier des positions relatives dans une image, telles que des décalages d’image ou des paramètres de recadrage, normalisées selon la taille de l’image.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>décalage de coordonnée normalisé à la taille d’une image (réel, réel) </p></td> 
 </tr> 
</table>

Les valeurs positives se déplacent vers le bas à droite.

Dans de nombreux cas, la position de référence est le centre de l’image. Dans ce cas, 0,0 correspond au centre de l’image, -0,5,-0,5 au coin supérieur gauche et 0,5,0,5 au coin inférieur droit.

Également utilisé pour spécifier les tailles d’image ou la taille du rectangle par rapport à la taille du calque 0. Dans ce cas, les valeurs doivent être supérieures à 0. 0 peut indiquer qu’une valeur par défaut spécifique doit être utilisée. 1,1 spécifie une taille égale à celle du calque 0.
