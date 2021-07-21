---
description: Publie les métadonnées sur le serveur de métadonnées.
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API,Métadonnées
role: Developer,Admin
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '71'
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
   <td colname="col3">Définissez cette variable sur <span class="codeph"> True</span> pour publier à nouveau toutes les <i>données </i> sur le serveur de métadonnées. <p>Remarque :  Selon la quantité de données, cette opération peut prendre plusieurs minutes à quelques heures. </p><p>Ne définissez pas ce paramètre si vous souhaitez publier des métadonnées nouvelles ou modifiées uniquement. </p></td> 
  </tr> 
 </tbody> 
</table>
