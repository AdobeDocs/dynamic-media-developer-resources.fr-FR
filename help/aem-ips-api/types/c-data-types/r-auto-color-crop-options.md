---
description: Options de recadrage automatique des images en fonction de la couleur.
seo-description: Options de recadrage automatique des images en fonction de la couleur.
seo-title: Options de recadrage automatique des couleurs
solution: Experience Manager
title: Options de recadrage automatique des couleurs
topic: Scene7 Image Production System API
uuid: 632ae721-7b39-4cd1-a1c6-1a3554167a4e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 12%

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
   <td colname="col2"> <span class="codeph"> xsd:doublon</span> </td> 
   <td colname="col3">Spécification des correspondances de couleurs. Utilisations : 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 pour correspondre exactement aux couleurs. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 pour activer le plus grand nombre de différences de couleur. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

