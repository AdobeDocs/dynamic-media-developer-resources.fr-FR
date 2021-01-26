---
description: Envoyez un nouveau traitement par lots.
seo-description: Envoyez un nouveau traitement par lots.
seo-title: batchjobsubmit
solution: Experience Manager
title: batchjobsubmit
topic: Dynamic Media Image Serving - Image Rendering API
uuid: eb695666-fcaf-40bc-8b56-452819f058d2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '44'
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
