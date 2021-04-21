---
description: Rappels de événement
solution: Experience Manager
title: Rappels de événement
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '221'
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

* `quickViewActivate` - se déclenche lorsqu’un utilisateur clique ou appuie sur une nuance interactive dans le composant de nuances interactives ou dans l’écran &quot;appel à l’action&quot; affiché à la fin de la lecture vidéo. Le gestionnaire de rappel prend le seul argument qui est un objet JSON avec les champs suivants :

   * `sku` {  `String`} valeur SKU associée à l’échantillon interactif.
   * `<additionalVariable>` {  `String`} zéro ou plusieurs variables supplémentaires associées à l’échantillon interactif.

Voir aussi [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) et [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
