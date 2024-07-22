---
title: Rappels d’événement
description: Rappels d’événement
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 24ea35c0-a0b1-4768-9336-94eb5e2d4fb2
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Rappels d’événement{#event-callbacks}

La visionneuse prend en charge les rappels d’événement JavaScript que la page web utilise pour suivre le processus d’initialisation de la visionneuse ou le comportement d’exécution.

Les gestionnaires de rappel sont affectés en transmettant des noms d’événement et des fonctions de gestionnaire correspondantes avec la propriété `handlers` à l’objet JSON `config` dans le constructeur de la visionneuse. Vous pouvez également utiliser la méthode d’API `setHandlers()`.

Les événements de visionneuse pris en charge sont les suivants :

* `initComplete` - se déclenche lorsque l’initialisation de la visionneuse est terminée et que tous les composants internes sont créés, de sorte qu’il est possible d’utiliser l’API `getComponent()`. Le gestionnaire de rappel ne prend aucun argument.
* `trackEvent` : se déclenche chaque fois qu’un événement se produit dans la visionneuse et qu’il peut être géré par un système de suivi des événements, tel qu’Adobe Analytics. Le gestionnaire de rappel utilise les arguments suivants :

   * `objID {String}` non utilisé actuellement.
   * `compClass {String}` non utilisé actuellement.
   * `instName {String}` nom d’instance du composant SDK de visionneuse HTML5 qui a déclenché l’événement.
   * Horodatage de l’événement `timeStamp {Number}`.
   * Charge utile de l’événement `eventInfo {String}`.

