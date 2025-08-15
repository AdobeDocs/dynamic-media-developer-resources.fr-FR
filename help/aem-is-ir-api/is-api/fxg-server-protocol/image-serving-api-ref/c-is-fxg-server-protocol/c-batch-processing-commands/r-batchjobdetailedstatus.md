---
description: Récupère le statut détaillé d’une tâche envoyée.
solution: Experience Manager
title: batchjobdetailedstatus
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd385327-29af-448c-9a25-75098b578272
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 2%

---

# batchjobdetailedstatus{#batchjobdetailedstatus}

Récupère le statut détaillé d’une tâche envoyée.

Ce paramètre :

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> du jobid </span> </p> </td> 
  <td class="stentry"> <p>Identifiant de tâche obtenu au moment de l’envoi. </p> </td> 
 </tr> 
</table>

Renvoie :

Statut détaillé du traitement au format XML ; erreur si `jobid` n’est pas valide ou si le traitement a été supprimé.

## Exemple {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
