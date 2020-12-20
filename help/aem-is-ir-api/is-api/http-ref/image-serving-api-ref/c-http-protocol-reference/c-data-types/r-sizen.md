---
description: Taille normalisée. Utilisé pour spécifier les tailles d’image ou les tailles de rectangle, normalisé par rapport à la taille du calque 0 ou d’une autre image.
seo-description: Taille normalisée. Utilisé pour spécifier les tailles d’image ou les tailles de rectangle, normalisé par rapport à la taille du calque 0 ou d’une autre image.
seo-title: sizeN
solution: Experience Manager
title: sizeN
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# sizeN{#sizen}

Taille normalisée. Utilisé pour spécifier les tailles d’image ou les tailles de rectangle, normalisé par rapport à la taille du calque 0 ou d’une autre image.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>largeur et hauteur normalisées par rapport à une autre image (réelle, réelle, supérieure à 0) </p></td> 
 </tr> 
</table>

*nx* et *ny* doivent être supérieurs à 0. 0,0 peut indiquer qu’une taille par défaut spécifique doit être utilisée. 1,1 indique une taille égale à l’image de référence.
