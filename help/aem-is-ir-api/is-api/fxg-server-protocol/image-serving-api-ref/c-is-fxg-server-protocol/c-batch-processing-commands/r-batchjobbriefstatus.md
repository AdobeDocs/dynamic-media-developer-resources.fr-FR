---
description: Récupérez l’état résumé d’une tâche envoyée.
solution: Experience Manager
title: batchjobstatus
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 1b31bdbb-3c2c-4f7f-ba95-d3e710270be0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 1%

---

# batchjobstatus{#batchjobbriefstatus}

Récupérez l’état résumé d’une tâche envoyée.

Ce paramètre :

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>Identifiant de tâche obtenu au moment de l’envoi. </p> </td> 
 </tr> 
</table>

Renvoie :

Bref état de la tâche au format XML; erreur si jobid n’est pas valide ou la tâche a été supprimée.

## Exemple {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
