---
description: 'null'
seo-description: 'null'
seo-title: 'Rappels de '
solution: Experience Manager
title: 'Rappels de '
topic: Dynamic media
uuid: 696838d2-11e4-4ef8-9cd3-136c5d5f6ed9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Rappels de{#event-callbacks}

Le lecteur prend en charge les rappels de JavaScript que la page Web utilise pour suivre le processus d’initialisation ou le comportement d’exécution de la visionneuse.

Les gestionnaires de rappel sont affectés en transmettant des noms de  de et des fonctions de gestionnaire correspondantes avec la `handlers` propriété à l’objet `config` JSON dans le constructeur du lecteur. Vous pouvez également utiliser la méthode `setHandlers()` API.

Les  de lecteur de contenu prises en charge sont les suivantes :

* `initComplete` - se déclenche lorsque l’initialisation du lecteur est terminée et que tous les composants internes sont créés, de sorte qu’il est possible d’utiliser `getComponent()` l’API. Le gestionnaire de rappel ne prend aucun argument.

* `trackEvent` - se déclenche chaque fois qu’un se produit dans la visionneuse, ce qui peut être géré par un système de suivi de  de, tel qu’Adobe Analytics. Le gestionnaire de rappel utilise les arguments suivants :

   * `objID {String}` non utilisé actuellement.
   * `compClass {String}` non utilisé actuellement.
   * `instName {String}` nom d’instance du composant SDK de la visionneuse qui a déclenché le .
   * `timeStamp {Number}` Horodatage .
   * `eventInfo {String}`  charge utile.

Voir aussi [MixedMediaViewer](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-mixedmediaviewer.md#reference-59b70dd7b58c43059bd85e3295441195) et [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-sethandlers.md#reference-09523cf4f448400b83f7906688368bf3).
