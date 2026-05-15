---
description: Tous les fichiers journaux sont écrits dans le même dossier de journal que celui spécifié par le répertoire TC.
solution: Experience Manager
title: Journalisation du serveur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
TQID: 'https://experienceleague.adobe.com/9I1gAXWb1Rpuml9WCCVPVC7FrpVazWN79Sk0-bb-tDc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 1%

---

# Journalisation du serveur{#server-logging}

Tous les fichiers journaux sont écrits dans le même dossier de journal que celui spécifié par TC::directory.

Les fichiers journaux sont généralement créés et pivotés quotidiennement. Les fichiers journaux plus anciens du dossier de journal sont automatiquement supprimés après un nombre de jours spécifié ( `TC::maxDays`).

Important : une quantité suffisante d’espace disque doit être réservée aux fichiers journaux pour éviter de manquer d’espace disque. 1 à 2 Go/jour peuvent être requis pour un serveur fortement utilisé et pour les paramètres de journal par défaut.

Le [!DNL Platform Server] et le serveur d’images créent les trois types de fichiers journaux décrits ci-dessous.

D’autres composants de diffusion d’images et certains autres packages Dynamic Media, tels que les visionneuses Dynamic Media, peuvent également créer des fichiers journaux dans le même dossier. Ces fichiers journaux sont destinés à une utilisation interne par Dynamic Media et peuvent être demandés par le support technique de Dynamic Media à des fins de dépannage.

* [Journal d’accès](c-access-log.md)
* [Log de trace](c-trace-log.md)
* [Journal du serveur d’images](c-image-server-log.md)

## Voir aussi {#section-5ff5e46031b1461c92de24e632610d6d}

[Journalisation des accès](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), [Journalisation du débogage/suivi](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
