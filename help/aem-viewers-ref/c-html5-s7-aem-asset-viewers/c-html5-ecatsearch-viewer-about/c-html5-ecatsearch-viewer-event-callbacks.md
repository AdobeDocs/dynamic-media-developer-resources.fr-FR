---
description: Rappels de événement
solution: Experience Manager
title: Rappels de événement
topic: Dynamic media
uuid: 0c4c4111-5ad7-458c-afa2-d551b5987322
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Rappels de événement{#event-callbacks}

Le lecteur prend en charge les rappels de événement JavaScript que la page Web utilise pour suivre le processus d’initialisation ou le comportement d’exécution de la visionneuse.

Les gestionnaires de rappel sont affectés en transmettant des noms de événement et des fonctions de gestionnaire correspondantes avec la propriété `handlers` à l’objet JSON `config` dans le constructeur de la visionneuse. Vous pouvez également utiliser la méthode API `setHandlers()`.

Les événements de lecteur pris en charge sont les suivants :

* `initComplete` - se déclenche lorsque l’initialisation de la visionneuse est terminée et que tous les composants internes sont créés, afin qu’il soit possible d’utiliser  `getComponent()` l’API. Le gestionnaire de rappel ne prend aucun argument.

* `trackEvent` - se déclenche chaque fois qu’un événement se produit dans la visionneuse et peut être géré par un système de suivi de événement, tel que Adobe Analytics. Le gestionnaire de rappel prend les arguments suivants :

   * `objID {String}` n’est pas actuellement utilisé.
   * `compClass {String}` n’est pas actuellement utilisé.
   * `instName {String}` nom d’instance du composant SDK de visionneuse qui a déclenché le événement.
   * `timeStamp {Number}` Horodatage événement.
   * `eventInfo {String}` Charge utile du événement.

Voir aussi [Visionneuse de catalogue électronique](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-javascriptapiref/r-html5-ecatsearch-javascriptapiref-ecatalogsearchviewer.md) et [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856).
