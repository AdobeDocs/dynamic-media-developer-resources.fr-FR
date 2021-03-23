---
description: Publie les métadonnées sur le serveur de métadonnées.
seo-description: Publie les métadonnées sur le serveur de métadonnées.
seo-title: MetadataPublishJobType
solution: Experience Manager
title: MetadataPublishJobType
uuid: 14cbb67e-56dc-4a25-b871-740be7ea7858
feature: Dynamic Media Classic, SDK/API, Métadonnées
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 8%

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

