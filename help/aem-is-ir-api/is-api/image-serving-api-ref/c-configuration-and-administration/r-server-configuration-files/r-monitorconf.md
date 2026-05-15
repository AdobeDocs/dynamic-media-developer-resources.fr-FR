---
description: Contient les paramètres du système de surveillance/d’alerte.
solution: Experience Manager
title: monitor.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 09c30680-dd9f-4744-b5ec-105721058883
TQID: 'https://experienceleague.adobe.com/xln1mw8Nx10vZMAf8Nu3K3V0CYh4c5Aajj5VWIoUs6s'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 0%

---

# monitor.conf{#monitor-conf}

Contient les paramètres du système de surveillance/d’alerte.

Ce fichier est un fichier de propriétés JAVA. Il faut veiller à respecter les conventions appropriées, faute de quoi la [!DNL Platform Server] risque de ne pas démarrer. Notez en particulier qu’une double barre oblique inverse « \ » ou une simple barre oblique inverse « / » doit être utilisée au lieu d’une barre oblique inverse « \ » dans les chemins d’accès aux fichiers Windows, car la barre oblique inverse est utilisée comme caractère d’échappement dans ce type de fichier.

Les modifications apportées à ce fichier prennent effet peu de temps après son enregistrement.

<table id="simpletable_91557E1162FF4FEC8BE1722D6656CFEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Généraux </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> monitorAlertGenerator.enableGlobalAlerting=false </span> </p> <p> <span class="codeph"> mailSender.host=127.0.0.1 </span> </p> <p> <span class="codeph"> mailSender.port=25 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageTo=noone@scene7.com </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageFrom=noone@scene7.com </span> </p> <p> <span class="codeph"> monitorAlertGenerator.alertInterval=600000 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.heapSpaceResetInterval=600000 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.minTrafficForAlerts=0.0 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Seuils d’alerte </p> </td> 
  <td class="stentry"> <p> monitorAlertGenerator.maxAverageResponseTime=200 </p> <p> monitorAlertGenerator.maxErrorRate=0.05 </p> <p> monitorAlertGenerator.minRequestRate=0.0 </p> <p> monitorAlertGenerator.minFreeHeapSpace=52428800 </p> <p> monitorAlertGenerator.maxOverlap=20 </p> <p> monitorAlertGenerator.lockedThreshold=60000 </p> </td> 
 </tr> 
</table>
