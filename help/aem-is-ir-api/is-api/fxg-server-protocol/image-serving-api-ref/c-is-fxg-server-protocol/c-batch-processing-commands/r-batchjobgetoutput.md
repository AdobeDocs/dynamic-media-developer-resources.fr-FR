---
description: Récupérez la sortie d’une tâche envoyée.
solution: Experience Manager
title: BatchJobGetOutput
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fb48c39-b15a-45b7-9aca-ed33f9c46c93
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 1%

---

# BatchJobGetOutput{#batchjobgetoutput}

Récupérez la sortie d’une tâche envoyée.

Ce paramètre :

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ID de jobid </span> </p> </td> 
  <td class="stentry"> <p>Identifiant de tâche obtenu au moment de la soumission. </p> </td> 
 </tr> 
</table>

Retourne:

La sortie PDF de la tâche est diffusée en réponse ; Si la tâche n’est pas valide ou si `jobid` la tâche a été supprimée.

## Exemple {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp ?req=batchjobgetoutput&amp;jobid=1005907604914d8eb63126b98f7172n76a5]
