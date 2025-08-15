---
description: Tous les fichiers journaux sont écrits dans le même dossier journal que celui du répertoire TC.
solution: Experience Manager
title: Journalisation du serveur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# Journalisation du serveur{#server-logging}

Tous les fichiers journaux sont écrits dans le même dossier journal que celui spécifié avec TC ::d irectory.

En règle générale, les fichiers journaux sont créés et font l’objet de rotations quotidiennes. Les anciens fichiers journaux du dossier journal sont automatiquement supprimés après un nombre spécifié de jours ( `TC::maxDays`).

Important Une quantité suffisante d’espace disque doit être réservée aux fichiers journaux pour éviter de manquer d’espace disque. 1 à 2 Go/jour peuvent être nécessaires pour un serveur très utilisé et les paramètres de journal par défaut.

Le [!DNL Platform Server] et le serveur d’images créent les trois types de fichiers journaux décrits ci-dessous.

D’autres composants Image Serving et certains autres packages Dynamic Media, tels que les visionneuses Dynamic Media, peuvent également créer des fichiers journaux dans le même dossier. Ces fichiers journaux sont destinés à Dynamic Media usage interne et peuvent être demandés par Dynamic Media support technique à des fins de dépannage.

* [Journal d’accès](c-access-log.md)
* [Journal de suivi](c-trace-log.md)
* [Journal du serveur d’images](c-image-server-log.md)

## Voir aussi {#section-5ff5e46031b1461c92de24e632610d6d}

[Journalisation](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f) des accès, journalisation [de débogage/suivi](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
