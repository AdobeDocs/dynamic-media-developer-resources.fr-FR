---
title: Rappels d’événement
description: Rappels d’événement
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 26f1dd99-fee9-4a71-9ec1-cfd1e29cb886
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Rappels d’événement{#event-callbacks}

La visionneuse prend en charge JavaScript rappels d’événement que la page Web utilise pour suivre le processus d’initialisation de la visionneuse ou le comportement d’exécution.

Les gestionnaires de rappel sont affectés en transmettant les noms d’événement et les fonctions de gestionnaire correspondantes avec la propriété à `handlers` l’objet `config` JSON dans le constructeur de la visionneuse. Il est également possible d’utiliser `setHandlers()` la méthode API.

Les événements de visionneuse pris en charge sont les suivants :

* `initComplete` - se déclenche lorsque l’initialisation de la visionneuse est terminée et que tous les composants internes sont créés, de sorte qu’il est possible d’utiliser `getComponent()` l’API. Le gestionnaire de rappel n’accepte aucun argument.

* `trackEvent` - se déclenche chaque fois qu’un événement se produit à l’intérieur de la visionneuse et peut être géré par un système de suivi d’événement, tel que Adobe Analytics. Le gestionnaire de rappel accepte les arguments suivants :

   * `objID {String}` Non utilisée actuellement.
   * `compClass {String}` Non utilisée actuellement.
   * `instName {String}` Nom d’occurrence du composant SDK de visionneuse qui a déclenché l’événement.
   * `timeStamp {Number}` Horodatage de l’événement.
   * `eventInfo {String}` Charge utile de l’événement.

Voir aussi [Visionneuse à 360°](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-spinviewer.md#reference-59b70dd7b58c43059bd85e3295441195) et [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-sethandlers.md#reference-d2223794fb45440094e9fdb5e9b73bef).
