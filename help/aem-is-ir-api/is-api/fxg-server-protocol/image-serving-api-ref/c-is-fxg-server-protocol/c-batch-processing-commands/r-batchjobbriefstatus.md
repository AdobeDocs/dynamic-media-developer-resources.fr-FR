---
description: Récupérer le statut résumé d'une tâche envoyée.
solution: Experience Manager
title: batchjobservistatus
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---


# batchjobservistatus{#batchjobbriefstatus}

Récupérer le statut résumé d&#39;une tâche envoyée.

Ce paramètre :

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>ID de tâche obtenu au moment de l’envoi. </p> </td> 
 </tr> 
</table>

Renvoie :

Bref état de la tâche au format XML ; si jobid n&#39;est pas valide ou si la tâche a été supprimée.

## Exemple {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
