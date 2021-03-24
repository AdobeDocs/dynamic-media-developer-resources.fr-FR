---
description: Envoyez un nouveau traitement par lots.
solution: Experience Manager
title: batchjobsubmit
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 2%

---


# batchjobsubmit{#batchjobsubmit}

Envoyez un nouveau traitement par lots.

Ce paramètre :

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata  </span> </p> </td> 
  <td class="stentry"> <p>Extrait XML des données de travail complètes. </p> </td> 
 </tr> 
</table>

Renvoie :

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Statut de la tâche </p> </td> 
  <td class="stentry"> <p>si la présentation a réussi ou échoué ; si la tâche a réussi, ID de la tâche au format XML. </p> </td> 
 </tr> 
</table>

## Exemple {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
