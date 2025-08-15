---
description: Envoyer un nouveau traitement par lots.
solution: Experience Manager
title: batchjobsubmit
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ab2f6e4-cd68-4f1e-ab54-6f5e9bfc87cb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '38'
ht-degree: 2%

---

# batchjobsubmit{#batchjobsubmit}

Envoyer un nouveau traitement par lots.

Ce paramètre :

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata </span> </p> </td> 
  <td class="stentry"> <p>Extrait de code XML des données de tâche complètes. </p> </td> 
 </tr> 
</table>

Renvoie :

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Statut du traitement </p> </td> 
  <td class="stentry"> <p>Indique si l’envoi a réussi ou échoué. En cas de succès, identifiant de tâche au format XML. </p> </td> 
 </tr> 
</table>

## Exemple {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
