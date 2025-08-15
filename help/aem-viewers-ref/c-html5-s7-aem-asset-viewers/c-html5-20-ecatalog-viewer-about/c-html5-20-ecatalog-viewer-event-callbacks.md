---
title: Rappels d’événement
description: Rappels d’événement
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7bd2e167-d04c-43e2-a71c-e2b3dddb13a0
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '147'
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
   * `timeStamp {Number}` l’horodatage de l’événement.
   * Payload d&#39;événement `eventInfo {String}`

Voir aussi [eCatalogViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-ecatalogviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) et [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856).
