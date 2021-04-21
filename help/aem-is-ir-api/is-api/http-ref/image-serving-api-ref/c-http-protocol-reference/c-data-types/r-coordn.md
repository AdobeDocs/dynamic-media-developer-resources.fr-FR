---
description: Coordonnées normalisées. Utilisé pour spécifier des positions relatives dans une image, telles que des décalages d’image ou des paramètres de recadrage, normalisés en fonction de la taille de l’image.
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '153'
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
