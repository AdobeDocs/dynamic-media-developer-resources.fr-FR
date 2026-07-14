---
description: Options de recadrage automatique des images en fonction de la couleur.
solution: Experience Manager
title: AutoColorCropOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 29d3dcfe-fddb-4806-b2aa-b96e9bbcff98
TQID: 'https://experienceleague.adobe.com/hQSiBufrm0h6lbwycT9KbgG1x6TGeCXa1t1DCL3hQQI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 46
ht-degree: 10%

---

# [!DNL AutoColorCropOptions]{#autocolorcropoptions}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> coin </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Choix du coin de recadrage automatique. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tolérance</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">Spécification de correspondance de couleurs. Utilise : <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 pour correspondre exactement aux couleurs. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 pour activer le plus de différences de couleurs. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

