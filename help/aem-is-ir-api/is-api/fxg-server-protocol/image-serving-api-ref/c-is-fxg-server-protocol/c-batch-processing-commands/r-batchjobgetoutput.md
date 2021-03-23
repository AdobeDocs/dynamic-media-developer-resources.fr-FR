---
description: Récupérez la sortie d’une tâche envoyée.
seo-description: Récupérez la sortie d’une tâche envoyée.
seo-title: batchjobgetoutput
solution: Experience Manager
title: batchjobgetoutput
uuid: c2d49cc2-3223-4f0f-8ba7-4f74a5f76789
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 1%

---


# batchjobgetoutput{#batchjobgetoutput}

Récupérez la sortie d’une tâche envoyée.

Ce paramètre :

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>ID de tâche obtenu au moment de l’envoi. </p> </td> 
 </tr> 
</table>

Renvoie :

La sortie PDF de la tâche est diffusée en continu en réponse à cette demande ; si `jobid` n&#39;est pas valide ou si la tâche a été supprimée.

## Exemple {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobgetoutput&jobid=1005907604914d8eb63126b98f7172n76a5]
