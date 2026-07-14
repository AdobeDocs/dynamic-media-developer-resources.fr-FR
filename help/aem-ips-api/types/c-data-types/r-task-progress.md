---
description: Informations sur l’avancement de la tâche.
solution: Experience Manager
title: ProgressionTâche
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 35e3be1e-ccc2-460c-98c1-bbefab1df699
TQID: 'https://experienceleague.adobe.com/uPZaPjWMBW4w2zyJ0nYIEiIrK8HIlE6sg2QKd3oDIC4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 3%

---

# [!DNL TaskProgress]{#taskprogress}

Informations sur l’avancement de la tâche.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Description du type de tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcesses</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nombre d'éléments de tâche déjà traités. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nombre d'éléments de tâche actuellement en cours. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numPending </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nombre d'éléments de tâche en attente (non encore traités). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progression </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> % de progression (plage 0,0 - 1,0). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Message de progression. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Heure de la dernière mise à jour des informations de progression. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TaskItemProgressArray</span> </td> 
   <td colname="col3"> Tableau d’éléments de tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskState </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Les valeurs sont les suivantes : 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> Inconnu </span> : lorsque le moniteur de tâche passe d’un état à l’autre. </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> Nouveau </span> : le moniteur de tâches a été créé mais n'a pas encore accepté de tâches. </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> des tâches </span> : le moniteur de tâches traite activement des tâches. </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> arrêt </span> : le moniteur de tâches arrête une tâche en raison d’une demande d’arrêt de tâche. </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> Terminé </span> : les tâches affectées aux tâches du moniteur de tâche sont terminées. </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> en échec </span> : indique une erreur irrécupérable. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

