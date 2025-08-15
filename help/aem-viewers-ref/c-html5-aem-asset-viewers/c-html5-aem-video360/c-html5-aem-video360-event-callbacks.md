---
title: Rappels d’événement
description: Rappels d’événement
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 24ea35c0-a0b1-4768-9336-94eb5e2d4fb2
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '148'
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
   * `instName {String}` le nom d’instance du composant SDK de la visionneuse HTML5 qui a déclenché l’événement.
   * `timeStamp {Number}` l’horodatage de l’événement.
   * Payload d’événement `eventInfo {String}`.

Voir aussi [Video360Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-video360viewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) et [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
