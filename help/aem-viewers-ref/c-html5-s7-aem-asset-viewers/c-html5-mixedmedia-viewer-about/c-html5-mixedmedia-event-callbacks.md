---
description: Rappels de événement
solution: Experience Manager
title: Rappels de événement
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '159'
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

Voir aussi [MixedMediaViewer](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-mixedmediaviewer.md#reference-59b70dd7b58c43059bd85e3295441195) et [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-sethandlers.md#reference-09523cf4f448400b83f7906688368bf3).
