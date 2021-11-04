---
title: Event callbacks
description: Rappels d’événement
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: f4db71f503749f086c86353578afe9dc368d04ae
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# Rappels d’événement{#event-callbacks}

The viewer supports JavaScript event callbacks that the web page uses to track the viewer initialization process or runtime behavior.

Les gestionnaires de rappel sont affectés en transmettant les noms d’événement et les fonctions de gestionnaire correspondantes avec `handlers` de `config` Objet JSON dans le constructeur de la visionneuse. Vous pouvez également utiliser `setHandlers()` méthode API.

Les événements de visionneuse pris en charge sont les suivants :

* `initComplete` - triggers when viewer initialization is complete and all internal components are created, so that it is possible to use `getComponent()` API. Le gestionnaire de rappel ne prend aucun argument.

* `trackEvent` - triggers each time an event occurs inside the viewer which may be handled by an event tracking system, such as Adobe Analytics. Le gestionnaire de rappel utilise les arguments suivants :

   * `objID {String}` not currently used.
   * `compClass {String}` not currently used.
   * `instName {String}` nom d’instance du composant SDK de la visionneuse qui a déclenché l’événement.
   * `eventInfo {String}` payload d’événement.

Voir aussi [SmartCropVideoViewer]
(/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md) et [setHandlers](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-sethandlers.md).
