---
description: Publie les métadonnées sur le serveur de métadonnées.
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
TQID: 'https://experienceleague.adobe.com/IMfUQ7SkEtpEmJrtyHzRm23OiC-zObGlEsnfRBWpTbo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 63
ht-degree: 7%

---

# [!DNL MetadataPublishJobType]{#metadatapublishjobtype}

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
   <td colname="col3">Définissez sur <span class="codeph"> True </span> pour publier à nouveau <i>toutes</i> les données sur le serveur de métadonnées. <p>Remarque : selon la quantité de données, cette opération peut prendre de quelques minutes à quelques heures. </p><p>Ne définissez pas ce paramètre si vous souhaitez publier uniquement les métadonnées nouvelles ou modifiées. </p></td> 
  </tr> 
 </tbody> 
</table>

