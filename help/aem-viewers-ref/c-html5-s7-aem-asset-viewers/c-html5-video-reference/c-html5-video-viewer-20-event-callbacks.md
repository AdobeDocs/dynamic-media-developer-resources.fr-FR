---
description: 'null'
seo-description: 'null'
seo-title: 'Rappels de '
solution: Experience Manager
title: 'Rappels de '
topic: Dynamic media
uuid: 08756e93-2c6c-4c63-9dd0-c64531561d6f
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

Voir aussi [Visionneuse](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-videoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) vidéo [et gestionnaires de](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-sethandlers.md#reference-22b373b37e8943a7be5c4d4cc21ed926)visionneuse.
