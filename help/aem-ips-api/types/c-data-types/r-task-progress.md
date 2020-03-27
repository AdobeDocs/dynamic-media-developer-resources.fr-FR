---
description: ' des informations de progression.'
seo-description: ' des informations de progression.'
seo-title: TaskProgress
solution: Experience Manager
title: TaskProgress
topic: Scene7 Image Production System API
uuid: b3b67803-147a-48a3-acc3-d608e01e0800
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TaskProgress{#taskprogress}

 des informations de progression.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Description du type . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcédé</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nombre d’éléments  déjà traités. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nombre d’éléments  en cours de traitement. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numPending</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nombre d’éléments de  en attente (non encore traités). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progression</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:</span> </td> 
   <td colname="col3"> % de progression (plage de 0,0 à 1,0). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Message de progression. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Heure de la dernière mise à jour des informations de progression. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:TaskItemProgressArray</span> </td> 
   <td colname="col3"> Tableau d’éléments . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tâcheÉtat</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Les valeurs sont les suivantes : 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> Inconnu</span>: Lorsque le contrôle le  entre les états. </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> Nouveau</span>:  moniteur a été créé mais n'a pas encore accepté le . </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> Traitement</span>:  moniteur de traite activement les  de. </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> Arrêt</span>:  moniteur de interrompt une tâche en raison d’une demande d’arrêt de tâche. </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> Terminé</span>: Les tâches affectées aux tâches de  de surveillance des ont été terminées. </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> Échec</span>: Indique une erreur fatale. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

