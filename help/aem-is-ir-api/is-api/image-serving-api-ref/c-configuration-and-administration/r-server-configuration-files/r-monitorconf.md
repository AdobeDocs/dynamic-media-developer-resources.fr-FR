---
description: Contient les paramètres du système de surveillance/alerte.
seo-description: Contient les paramètres du système de surveillance/alerte.
seo-title: monitor.conf
solution: Experience Manager
title: monitor.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: 31949797-df2c-4b7c-841b-4c623299a228
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# monitor.conf{#monitor-conf}

Contient les paramètres du système de surveillance/alerte.

Ce fichier est un fichier de propriétés JAVA. Il faut veiller à respecter les conventions appropriées ; dans le cas contraire, le serveur de plateformes risque de ne pas être en début. Notez en particulier qu&#39;une barre oblique inverse de doublon &quot;\\&quot; ou une barre oblique inverse &quot;/&quot; doit être utilisée à la place d&#39;une barre oblique inverse &quot;\&quot; dans les chemins d&#39;accès aux fichiers Windows, puisque la barre oblique inverse est utilisée comme caractère d&#39;échappement dans ce type de fichier.

Les modifications apportées à ce fichier prennent effet peu de temps après leur enregistrement.

<table id="simpletable_91557E1162FF4FEC8BE1722D6656CFEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Généraux </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> monitorAlertGenerator.enableGlobalAlerting=false  </span> </p> <p> <span class="codeph"> mailSender.host=127.0.0.1  </span> </p> <p> <span class="codeph"> mailSender.port=25  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageTo=noone@scene7.com  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageFrom=noone@scene7.com  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.alertInterval=600000  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.heapSpaceResetInterval=600000  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.minTrafficForAlerts=0.0  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Seuils d'alerte </p> </td> 
  <td class="stentry"> <p> monitorAlertGenerator.maxAverageResponseTime=200 </p> <p> monitorAlertGenerator.maxErrorRate=0.05 </p> <p> monitorAlertGenerator.minRequestRate=0.0 </p> <p> monitorAlertGenerator.minFreeHeapSpace=52428800 </p> <p> monitorAlertGenerator.maxOverlap=20 </p> <p> monitorAlertGenerator.lockedThreshold=60000 </p> </td> 
 </tr> 
</table>

