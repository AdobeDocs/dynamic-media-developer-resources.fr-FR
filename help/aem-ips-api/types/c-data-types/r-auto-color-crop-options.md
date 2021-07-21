---
description: Options de recadrage automatique des images en fonction de la couleur.
solution: Experience Manager
title: AutoColorCropOptions
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 29d3dcfe-fddb-4806-b2aa-b96e9bbcff98
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 13%

---

# AutoColorCropOptions{#autocolorcropoptions}

Options de recadrage automatique des images en fonction de la couleur.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> corner</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Choix du coin de recadrage automatique. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tolérance</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">Spécification de correspondance des couleurs. Utilise : 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 pour faire correspondre exactement les couleurs. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 pour activer le plus grand nombre de différences de couleurs. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
