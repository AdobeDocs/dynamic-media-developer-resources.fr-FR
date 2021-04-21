---
description: Publie les métadonnées sur le serveur de métadonnées.
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 9%

---


# MetadataPublishJobType{#metadatapublishjobtype}

Publie les métadonnées sur le serveur de métadonnées.

Syntaxe

## Paramètres {#section-6c51fa689b3648fbb7c7945a7e176d0a}

<table id="table_23B5CFC5C3F946F9AFDB6A83A1AAB7AF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> forcePublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Définissez cette variable sur <span class="codeph"> True</span> pour publier à nouveau <i>toutes</i> les données sur le serveur de métadonnées. <p>Remarque :  En fonction de la quantité de données, cette opération peut prendre plusieurs minutes à quelques heures. </p><p>Ne définissez pas ce paramètre si vous souhaitez publier uniquement des métadonnées nouvelles ou modifiées. </p></td> 
  </tr> 
 </tbody> 
</table>

