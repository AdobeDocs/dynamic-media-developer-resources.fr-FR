---
description: Contient les paramètres du système de surveillance/alerte.
solution: Experience Manager
title: monitor.conf
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 09c30680-dd9f-4744-b5ec-105721058883
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# monitor.conf{#monitor-conf}

Contient les paramètres du système de surveillance/alerte.

Ce fichier est un fichier de propriétés JAVA. Il faut veiller à respecter les conventions appropriées ; dans le cas contraire, il se peut que le serveur Platform ne démarre pas. Notez en particulier qu’une double barre oblique inverse &quot;\\&quot; ou une seule barre oblique inverse &quot;/&quot; doit être utilisée à la place d’une barre oblique inverse &quot;\&quot; dans les chemins d’accès aux fichiers Windows, car la barre oblique inverse est utilisée comme caractère d’échappement dans ce type de fichier.

Les modifications apportées à ce fichier prennent effet peu de temps après l’enregistrement du fichier.

<table id="simpletable_91557E1162FF4FEC8BE1722D6656CFEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Généraux </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> monitorAlertGenerator.enableGlobalAlerting=false  </span> </p> <p> <span class="codeph"> mailSender.host=127.0.0.1  </span> </p> <p> <span class="codeph"> mailSender.port=25  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageTo=noone@scene7.com  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageFrom=noone@scene7.com  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.alertInterval=600000  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.heapSpaceResetInterval=600000  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.minTrafficForAlerts=0.0  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Seuils d’alerte </p> </td> 
  <td class="stentry"> <p> monitorAlertGenerator.maxAverageResponseTime=200 </p> <p> monitorAlertGenerator.maxErrorRate=0.05 </p> <p> monitorAlertGenerator.minRequestRate=0.0 </p> <p> monitorAlertGenerator.minFreeHeapSpace=52428800 </p> <p> monitorAlertGenerator.maxOverlap=20 </p> <p> monitorAlertGenerator.lockedThreshold=60000 </p> </td> 
 </tr> 
</table>
