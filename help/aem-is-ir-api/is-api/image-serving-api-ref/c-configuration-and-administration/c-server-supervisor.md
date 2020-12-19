---
description: Les composants Image Serving sont gérés par le Contrôleur de serveur, qui est un démon Linux ou un service Windows (S7Supervisor.exe, répertorié comme "Service d’image Scene7" dans le Panneau de Contrôle Services).
seo-description: Les composants Image Serving sont gérés par le Contrôleur de serveur, qui est un démon Linux ou un service Windows (S7Supervisor.exe, répertorié comme "Service d’image Scene7" dans le Panneau de Contrôle Services).
seo-title: Responsable du serveur
solution: Experience Manager
title: Responsable du serveur
topic: Scene7 Image Serving - Image Rendering API
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Responsable du serveur{#server-supervisor}

Les composants Image Serving sont gérés par le Contrôleur de serveur, qui est un démon Linux ou un service Windows (S7Supervisor.exe, répertorié comme &quot;Service d’image Scene7&quot; dans le Panneau de Contrôle Services).

En plus de démarrer et d’arrêter d’autres composants de diffusion d’images, le responsable du serveur est responsable de l’intégrité de ces autres composants. Si un composant se bloque, il est automatiquement redémarré afin de minimiser les interruptions de service.

## Démarrage et arrêt de {#section-061d28d74e034a30adc39ea3e2031cd0}

Le contrôleur de serveur est démarré, arrêté et redémarré avec le script de l’utilitaire Image Serving. Pour plus d&#39;informations, consultez la [documentation Utilitaires](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f).

Le démarrage et l’arrêt du superviseur de serveur début automatiquement et arrête tous les autres composants de la diffusion d’images.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
