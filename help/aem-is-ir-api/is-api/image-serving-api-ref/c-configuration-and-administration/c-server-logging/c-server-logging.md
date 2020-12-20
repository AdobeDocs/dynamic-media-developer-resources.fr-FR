---
description: Tous les fichiers journaux sont écrits dans le même dossier de journaux que celui spécifié dans le répertoire TC.
seo-description: Tous les fichiers journaux sont écrits dans le même dossier de journaux que celui spécifié dans le répertoire TC.
seo-title: Journalisation du serveur
solution: Experience Manager
title: Journalisation du serveur
topic: Scene7 Image Serving - Image Rendering API
uuid: f6145737-e4c3-4533-9be5-5b5a0202fe33
translation-type: tm+mt
source-git-commit: 5717550d2dea8ec086875e770ff8f200aaa75ff3
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---


# Journalisation du serveur {#server-logging}

Tous les fichiers journaux sont écrits dans le même dossier de journaux que celui spécifié dans le répertoire TC::directory.

Les fichiers journaux sont généralement créés et pivotés quotidiennement. Les fichiers journaux plus anciens du dossier de journalisation sont automatiquement supprimés après un nombre spécifié de jours ( `TC::maxDays`).

Important Un espace disque suffisant doit être réservé aux fichiers journaux pour éviter de manquer d&#39;espace disque. 1 à 2 Go/jour peut être nécessaire pour un serveur très utilisé et pour les paramètres de journal par défaut.

Platform Server et Image Server créent les trois types de fichiers journaux décrits ci-dessous.

D’autres composants de diffusion d’images et certains autres packages Scene7, tels que les visionneuses Scene7, peuvent également créer des fichiers journaux dans le même dossier. Ces fichiers journaux sont destinés à un usage interne de Scene7 et peuvent être demandés par l&#39;assistance Scene7 à des fins de dépannage.

* [Journal d’accès](c-access-log.md)
* [Journal de suivi](c-trace-log.md)
* [Journal du serveur d’images](c-image-server-log.md)

## Voir aussi {#section-5ff5e46031b1461c92de24e632610d6d}

[Journalisation](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f) des accès,  [débogage/suivi](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
