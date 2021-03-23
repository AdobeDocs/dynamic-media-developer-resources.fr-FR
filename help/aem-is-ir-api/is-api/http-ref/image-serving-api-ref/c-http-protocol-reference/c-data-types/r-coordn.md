---
description: Coordonnées normalisées. Utilisé pour spécifier des positions relatives dans une image, telles que des décalages d’image ou des paramètres de recadrage, normalisés en fonction de la taille de l’image.
seo-description: Coordonnées normalisées. Utilisé pour spécifier des positions relatives dans une image, telles que des décalages d’image ou des paramètres de recadrage, normalisés en fonction de la taille de l’image.
seo-title: coordN
solution: Experience Manager
title: coordN
uuid: e182650b-aff6-4dd2-8edb-cd0d361865fd
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# coordN{#coordn}

Coordonnées normalisées. Utilisé pour spécifier des positions relatives dans une image, telles que des décalages d’image ou des paramètres de recadrage, normalisés en fonction de la taille de l’image.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>décalage de coordonnées normalisé à la taille d’une image (réel, réel) </p></td> 
 </tr> 
</table>

Les valeurs positives se déplacent vers le coin inférieur droit.

Dans de nombreux cas, la position de référence est le centre de l’image. Dans ce cas, 0,0 correspond au centre de l’image, -0,5,-0,5 au coin supérieur gauche et 0,5,0,5 au coin inférieur droit.

Également utilisé pour spécifier les tailles d’image ou la taille du rectangle par rapport à la taille du calque 0. Dans ce cas, les valeurs doivent être supérieures à 0. 0 peut indiquer qu’une valeur par défaut spécifique doit être utilisée. 1,1 spécifie une taille égale à celle du calque 0.
