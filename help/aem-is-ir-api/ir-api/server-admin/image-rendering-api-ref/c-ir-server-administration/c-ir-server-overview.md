---
description: Cette documentation explique comment administrer le serveur de rendu d’image Dynamic Media.
solution: Experience Manager
title: Présentation de l’administration du serveur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
TQID: 'https://experienceleague.adobe.com/t9zGehwMxhHq1HrP3mmNGvkthmqYxX2ijeyihn5OEWI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# Présentation de l’administration du serveur{#server-administration-overview}

Cette documentation explique comment administrer le serveur de rendu d’image Dynamic Media.

Le rendu d’image se compose de deux composants principaux :

* Un package Java est déployé avec le [!DNL Platform Server] de diffusion d’images et gère la connexion client, la mise en cache et les catalogues de matériaux.
* Un module de code natif est déployé en tant que bibliothèque d’extension pour le serveur d’images et implémente les principales fonctionnalités de rendu d’image.

Les deux composants sont collectivement appelés *serveur de rendu*.

Le rendu d’image partage de nombreuses fonctionnalités de serveur avec le service d’images. Toutes les options sont configurées en modifiant un fichier de configuration. Des attributs de configuration supplémentaires sont fournis par le catalogue par défaut ( [!DNL default.ini]) ou par des catalogues de matières spécifiques. Voir Catalogues de matières pour plus de détails.

Le dossier d’installation du rendu d’image ( *[!DNL install_folder]*) est [!DNL *[!DNL install_root]*/ImageRendering]. Sous Windows, le *[!DNL install_root]* par défaut est `C:\Program Files\Scene7`. Un dossier différent peut être spécifié lors de l’installation. Sous Linux, *[!DNL install_root]* doit toujours être [!DNL /usr/local/scene7]. Des liens symboliques peuvent être utilisés.

Tous les chemins d’accès aux fichiers sont sensibles à la casse sous UNIX et insensibles à la casse sous Windows.

