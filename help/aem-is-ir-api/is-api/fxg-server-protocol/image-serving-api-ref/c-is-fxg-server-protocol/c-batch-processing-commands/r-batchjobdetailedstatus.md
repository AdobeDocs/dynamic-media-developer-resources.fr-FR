---
description: Récupère le statut détaillé d’une tâche envoyée.
solution: Experience Manager
title: batchjobdetailedstatus
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd385327-29af-448c-9a25-75098b578272
TQID: 'https://experienceleague.adobe.com/-KwrpZVglPaJUe2XKkpjej-Y8KG0X7VzGF-cR-m2rV8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 47
ht-degree: 2%

---

# batchjobdetailedstatus{#batchjobdetailedstatus}

Récupère le statut détaillé d’une tâche envoyée.

Ce paramètre :

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> du jobid <span class="codeph"> </p> </td> 
  <td class="stentry"> <p>Identifiant de tâche obtenu au moment de l’envoi. </p> </td> 
 </tr> 
</table>

Renvoie :

Statut détaillé du traitement au format XML ; erreur si `jobid` n’est pas valide ou si le traitement a été supprimé.

## Exemple {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
