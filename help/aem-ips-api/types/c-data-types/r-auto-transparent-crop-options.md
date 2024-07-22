---
description: Options utilisées lors du recadrage automatique d’images en fonction de la transparence.
solution: Experience Manager
title: AutoTransparentCropOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 351f63a4-cc1b-4db9-93df-c21acd02e12a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 10%

---

# [!DNL AutoTransparentCropOptions]{#autotransparentcropoptions}

Options utilisées lors du recadrage automatique d’images en fonction de la transparence.

Syntaxe

## Paramètres {#section-0302e9238dbc4704914e938f42c881e6}

<table id="table_F6A0DBA37F704C2097C617A0A6767566"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> tolérance</span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">Supprime l’espace blanc des bords de l’image en fonction de la transparence. Utilise : 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 pour faire correspondre exactement les couleurs. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 pour activer le plus grand nombre de différences de couleurs. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
