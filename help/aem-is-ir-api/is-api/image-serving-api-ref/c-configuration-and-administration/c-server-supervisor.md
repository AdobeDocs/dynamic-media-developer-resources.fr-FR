---
description: Les composants de diffusion d’images sont gérés par le responsable du serveur, qui est un démon Linux ou un service Windows (S7Supervisor.exe, répertorié comme "Service d’images Dynamic Media" dans le Panneau de Contrôle Services).
solution: Experience Manager
title: Superviseur du serveur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---

# Superviseur du serveur{#server-supervisor}

Les composants de diffusion d’images sont gérés par le responsable du serveur, qui est un démon Linux ou un service Windows (S7Supervisor.exe, répertorié comme &quot;Service d’images Dynamic Media&quot; dans le Panneau de Contrôle Services).

Outre le démarrage et l’arrêt d’autres composants du serveur d’images, le responsable du serveur est chargé d’assurer l’intégrité de ces autres composants. Si un composant se bloque, il est automatiquement redémarré afin de minimiser toute interruption de service.

## Démarrage et arrêt {#section-061d28d74e034a30adc39ea3e2031cd0}

Le responsable du serveur est démarré, arrêté et redémarré à l’aide du script de l’utilitaire de diffusion d’images. Pour plus d’informations, consultez la [documentation Utilities](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) .

Le démarrage et l’arrêt du superviseur du serveur démarre et arrête automatiquement tous les autres composants du serveur d’images.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
