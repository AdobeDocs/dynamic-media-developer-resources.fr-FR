---
description: 'null'
seo-description: 'null'
seo-title: 'Rappels de '
solution: Experience Manager
title: 'Rappels de '
topic: Dynamic media
uuid: 0c4c4111-5ad7-458c-afa2-d551b5987322
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

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

Voir aussi [Visionneuse](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-javascriptapiref/r-html5-ecatsearch-javascriptapiref-ecatalogsearchviewer.md) de catalogue électronique et gestionnaires de [visionneuses](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856).
