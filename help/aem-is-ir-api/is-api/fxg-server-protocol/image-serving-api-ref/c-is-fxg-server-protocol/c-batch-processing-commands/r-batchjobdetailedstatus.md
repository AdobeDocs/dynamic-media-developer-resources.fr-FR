---
description: Récupérez le statut détaillé d'une tâche envoyée.
solution: Experience Manager
title: batchjobdetailedstatus
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 1%

---


# batchjobdetailedstatus{#batchjobdetailedstatus}

Récupérez le statut détaillé d&#39;une tâche envoyée.

Ce paramètre :

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>ID de tâche obtenu au moment de l’envoi. </p> </td> 
 </tr> 
</table>

Renvoie :

Statut détaillé de la tâche au format XML ; si `jobid` n&#39;est pas valide ou si la tâche a été supprimée.

## Exemple {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
