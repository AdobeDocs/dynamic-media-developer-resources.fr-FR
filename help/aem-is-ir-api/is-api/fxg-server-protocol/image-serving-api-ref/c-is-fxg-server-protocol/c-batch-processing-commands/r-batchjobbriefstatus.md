---
title: batchjobbrief status
description: Récupère le statut résumé d’une tâche envoyée.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b31bdbb-3c2c-4f7f-ba95-d3e710270be0
TQID: 'https://experienceleague.adobe.com/la3dpm1US1LePnjyA1jbTG8aSNDrovP-GPFeJMwrYxI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 55
ht-degree: 1%

---

# batchjobbrief status{#batchjobbriefstatus}

Récupère le statut résumé d’une tâche envoyée.

Ce paramètre :

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> du jobid <span class="codeph"> </p> </td> 
  <td class="stentry"> <p>Identifiant de tâche obtenu au moment de l’envoi. </p> </td> 
 </tr> 
</table>

Renvoie :

État succinct du traitement au format XML ; erreur si l’ID de traitement n’est pas valide ou si le traitement a été supprimé.

## Exemple {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbrief&amp;jobid=1005907604914d8eb63126b98f7172n76a5]
