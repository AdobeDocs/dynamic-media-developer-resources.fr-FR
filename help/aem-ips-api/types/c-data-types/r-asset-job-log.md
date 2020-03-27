---
description: Détails d’une entrée de journal des tâches associée à une ressource particulière. Données renvoyées par getAssetJobLogs.
seo-description: Détails d’une entrée de journal des tâches associée à une ressource particulière. Données renvoyées par getAssetJobLogs.
seo-title: AssetJobLog
solution: Experience Manager
title: AssetJobLog
topic: Scene7 Image Production System API
uuid: 0dd65da1-f358-4d9a-98a2-abfb036347e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AssetJobLog{#assetjoblog}

Détails d’une entrée de journal des tâches associée à une ressource particulière. Données renvoyées par getAssetJobLogs.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> tâcheHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Poignée de tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nom de la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Message dans le journal des tâches. <p><span class="codeph"> Le champ de réponse logMessage</span> est localisé en fonction du champ de paramètre régional <span class="codeph"> authHeader</span> . </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Type de tâche dans l’entrée du journal. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> adresse électronique de l’utilisateur qui a envoyé la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logDate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Date de la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> auxArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:JobLogDetailArray</span> </td> 
   <td colname="col3"> Tableau de messages auxiliaires du journal des tâches pour chaque journal des tâches. </td> 
  </tr> 
 </tbody> 
</table>

