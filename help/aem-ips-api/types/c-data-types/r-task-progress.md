---
description: Informations sur l’avancement de la tâche.
solution: Experience Manager
title: Progression de la tâche
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 35e3be1e-ccc2-460c-98c1-bbefab1df699
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '139'
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
   <td colname="col1"> <span class="codeph"><span class="varname"> Type de tâche</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Description du type de tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> numProcessed</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :int</span> </td> 
   <td colname="col3"> Nombre d’éléments de tâche déjà traités. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Traitement</span> du num </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :int</span> </td> 
   <td colname="col3"> Nombre d’éléments de tâche en cours de traitement. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Numéro en attente</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :int</span> </td> 
   <td colname="col3"> Nombre d’éléments de tâche en attente (pas encore traités). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> progrès</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :double</span> </td> 
   <td colname="col3"> % d’avancement (intervalle de 0,0 à 1,0). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Message de</span> progression </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Message d’avancement. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Dernière mise à jour</span> des progrès </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :dateTime</span> </td> 
   <td colname="col3"> Heure de la dernière mise à jour des informations de progression. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> taskItemProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :TaskItemProgressArray</span> </td> 
   <td colname="col3"> Tableau d’éléments de tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> taskState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3">Les valeurs possibles sont : 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> Inconnu</span> : lorsque le moniteur de tâches passe d’un état à l’autre. </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> Nouveau</span> : Le moniteur de tâches a été créé, mais n’a pas encore accepté les tâches. </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> Traitement</span> : le moniteur de tâches traite activement les tâches. </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> Arrêt</span> : le moniteur de tâches arrête une tâche suite à une demande d’arrêt de la tâche. </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> Terminé</span> : les tâches affectées aux tâches de surveillance de tâche ont été terminées. </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> Échec</span> : indique une erreur irrécupérable. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
