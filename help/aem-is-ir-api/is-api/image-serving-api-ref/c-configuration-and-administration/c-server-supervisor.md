---
description: Les composants du serveur d’images sont gérés par le contrôleur de serveur, qui est un démon Linux ou un service Windows (S7Supervisor.exe, répertorié comme "Scene7 Image Serving" dans le Panneau de configuration des services).
seo-description: Les composants du serveur d’images sont gérés par le contrôleur de serveur, qui est un démon Linux ou un service Windows (S7Supervisor.exe, répertorié comme "Scene7 Image Serving" dans le Panneau de configuration des services).
seo-title: Responsable du serveur
solution: Experience Manager
title: Responsable du serveur
topic: Scene7 Image Serving - Image Rendering API
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Responsable du serveur{#server-supervisor}

Les composants du serveur d’images sont gérés par le contrôleur de serveur, qui est un démon Linux ou un service Windows (S7Supervisor.exe, répertorié comme &quot;Scene7 Image Serving&quot; dans le Panneau de configuration des services).

En plus de démarrer et d’arrêter d’autres composants de la diffusion d’images, le superviseur du serveur est responsable de l’intégrité de ces autres composants. En cas de panne d’un composant, il est automatiquement redémarré afin de minimiser les interruptions de service.

## Démarrage et arrêt {#section-061d28d74e034a30adc39ea3e2031cd0}

Le contrôleur du serveur est démarré, arrêté et redémarré avec le script de l’utilitaire Image Serving. See the [Utilities documentation](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) for more information.

Le démarrage et l’arrêt du contrôleur de serveur  automatiquement et interrompt tous les autres composants de la diffusion d’images.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
