---
description: Tous les fichiers journaux sont écrits dans le même dossier de journaux que celui spécifié dans le répertoire TC.
solution: Experience Manager
title: Journalisation du serveur
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# Journalisation du serveur{#server-logging}

Tous les fichiers journaux sont écrits dans le même dossier de logs que celui spécifié par TC::directory.

Les fichiers journaux sont généralement créés et pivotés quotidiennement. Les fichiers journaux plus anciens du dossier de journaux sont automatiquement supprimés après un nombre spécifié de jours ( `TC::maxDays`).

Important : Une quantité suffisante d’espace disque doit être réservée aux fichiers journaux pour éviter que l’espace disque ne manque. 1 à 2 Go/jour peut être nécessaire pour un serveur très utilisé et les paramètres de journal par défaut.

Platform Server et Image Server créent les trois types de fichiers journaux décrits ci-dessous.

D’autres composants de diffusion d’images et certains autres modules Dynamic Media, tels que les visionneuses Dynamic Media, peuvent également créer des fichiers journaux dans le même dossier. Ces fichiers journaux sont destinés à un usage interne de Dynamic Media et peuvent être demandés par le support technique de Dynamic Media à des fins de dépannage.

* [Journal d’accès](c-access-log.md)
* [Journal de suivi](c-trace-log.md)
* [Journal du serveur d’images](c-image-server-log.md)

## Voir aussi {#section-5ff5e46031b1461c92de24e632610d6d}

[Journalisation des accès](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f),  [débogage/suivi](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
