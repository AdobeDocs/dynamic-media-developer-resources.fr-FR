---
description: Taille normalisée. Utilisé pour spécifier les tailles d’image ou les tailles de rectangle, normalisées par rapport à la taille du calque 0 ou à une autre image.
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# sizeN{#sizen}

Taille normalisée. Utilisé pour spécifier les tailles d’image ou les tailles de rectangle, normalisées par rapport à la taille du calque 0 ou à une autre image.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>largeur et hauteur normalisées par rapport à une autre image (réelle, réelle, supérieure à 0) </p></td> 
 </tr> 
</table>

*nx* et *ny* doivent être postérieurs à 0. 0,0 peut indiquer qu’une taille par défaut spécifique doit être utilisée. 1,1 spécifie une taille égale à l’image de référence.
