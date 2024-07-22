---
title: AssetJobLog
description: Détails d’une entrée de journal de tâche associée à une ressource particulière. Données renvoyées par getAssetJobLogs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 2c8ebec2-a664-46cd-b843-9893bfa0a9d1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 5%

---

# [!DNL AssetJobLog]{#assetjoblog}

Détails d’une entrée de journal de tâche associée à une ressource particulière. Données renvoyées par getAssetJobLogs.

Syntaxe

## Paramètres {#section-5da4d6156b7f4ca88a67202fbf736104}

<table id="table_7BC785BC95EA43D582D1B2289FF3130D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL jobHandle]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Poignée de tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL jobName]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nom de la tâche </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL logMessage]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Message dans le journal de la tâche. <p>Le champ de réponse <span class="codeph"> [!DNL logMessage]</span> est localisé en fonction du champ du paramètre régional <span class="codeph"> authHeader</span> . </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL logType]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Type de tâche dans l’entrée de journal. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL submitUserEmail]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> courrier électronique de l’utilisateur qui a envoyé la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL logDate]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Date de la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL auxArray]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:JobLogDetailArray</span> </td> 
   <td colname="col3"> Tableau des messages du journal des tâches auxiliaire pour chaque journal des tâches. </td> 
  </tr> 
 </tbody> 
</table>
