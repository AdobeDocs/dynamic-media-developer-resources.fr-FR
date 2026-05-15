---
title: Rappels d’événement
description: Rappels d’événement
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
TQID: 'https://experienceleague.adobe.com/pAXI43BvGyX7rM3--kuoLsAsexeM993-WKoLPCU9Zzg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 210
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
   * Payload d’événement `eventInfo {String}`.

* `quickViewActivate` : se déclenche lorsqu’un utilisateur clique ou appuie sur une nuance interactive dans le composant nuancier interactif ou dans l’écran « call to action » affiché à la fin de la lecture vidéo. Le gestionnaire de rappel prend le seul argument qui est un objet JSON avec les champs suivants :

   * `sku` valeur de SKU { `String`} associée à l’échantillon interactif.
   * `<additionalVariable>` { `String`} aucune ou plusieurs variables supplémentaires associées à l’échantillon interactif.

Voir aussi [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) et [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
