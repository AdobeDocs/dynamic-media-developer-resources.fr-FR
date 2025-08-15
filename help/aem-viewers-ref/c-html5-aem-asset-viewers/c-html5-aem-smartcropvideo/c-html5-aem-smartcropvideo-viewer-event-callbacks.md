---
title: Rappels d’événement
description: Rappels d’événement
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 21962c01-f224-408d-8072-1c7f5d78ac4b
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Rappels d’événement{#event-callbacks}

La visionneuse prend en charge les rappels d’événement JavaScript que la page web utilise pour effectuer le suivi du processus d’initialisation de la visionneuse ou du comportement d’exécution.

Les gestionnaires de rappel sont attribués en transmettant les noms d’événement et les fonctions de gestionnaire correspondantes avec la propriété `handlers` à `config`’objet JSON dans le constructeur de la visionneuse. Il est également possible d’utiliser `setHandlers()` méthode API.

Les événements de visionneuse pris en charge sont les suivants :

* `initComplete` - se déclenche lorsque l’initialisation de la visionneuse est terminée et que tous les composants internes sont créés, de sorte qu’il soit possible d’utiliser l’API `getComponent()`. Le gestionnaire de rappel ne prend aucun argument.

* `trackEvent` : se déclenche chaque fois qu’un événement se produit dans la visionneuse, qui peut être géré par un système de suivi des événements, tel qu’Adobe Analytics. Le gestionnaire de rappel utilise les arguments suivants :

   * `objID {String}` non utilisé actuellement.
   * `compClass {String}` non utilisé actuellement.
   * `instName {String}` le nom d’instance du composant SDK de la visionneuse qui a déclenché l’événement.
   * Payload d’événement `eventInfo {String}`.

Voir aussi [SmartCropVideoViewer]
(/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md) et [setHandlers](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-sethandlers.md).
