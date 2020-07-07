---
description: Paramètres généraux du serveur
seo-description: Paramètres généraux du serveur
seo-title: Généraux
solution: Experience Manager
title: Généraux
topic: Scene7 Image Serving - Image Rendering API
uuid: d7ec3dba-64b8-431b-b446-84ab6139ba8a
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 1%

---


# Généraux{#general}

Paramètres généraux du serveur

## TC::PsPort - Port d’écoute principal {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Spécifie le port d’écoute principal pour le serveur Platform Server. Ce port permet également d’accéder à la documentation et aux exemples de pages relatifs à la diffusion d’images, au rendu des images et aux visionneuses Scene7 (si elles sont installées).

## IS::CacheServerUrl - URL racine du service de mise en cache {#section-bcca227a1f91453b834db4ea050968e2}

Spécifie le chemin d’accès racine HTTP pour permettre à Image Server d’accéder au service de mise en cache. Doit être défini sur [!DNL http://localhost:TC::PsPort /is/cache/secondary], avec le numéro de port correspondant `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - TTL par défaut de la source d&#39;image distante {#section-e4c31228b459492cacd2f482d9575f71}

TTL pour les images mises en cache obtenues via HTTP à partir d’une source distante utilisant le `src={…}` concept. Utilisé uniquement lorsque le serveur distant n’inclut pas d’en-tête Expiration dans sa réponse HTTP. Valeur entière en secondes.

## IS::RemoteUrlTimeout - Délai d’expiration de la source d’image distante {#section-437646c479cc4bea81dae42100a3c50a}

Heure à laquelle le serveur d’images attend qu’un serveur distant diffuse le fichier image demandé via HTTP avant de renvoyer une erreur. Valeur entière en secondes.

## PS::allowDefaultCatalogRequests - Activer/désactiver les requêtes de catalogue par défaut {#section-484e442a115a49b4ac269d1718b351e1}

Définissez cette variable sur false pour interdire les requêtes qui n’incluent pas d’ID de catalogue valide dans le chemin d’accès. Default is `true`. Lorsqu’elle est définie sur `false`, une erreur est renvoyée pour les requêtes sans ID de catalogue.

>[!NOTE]
>
>`req=catalogprops` n’est pas soumis à ce paramètre.

## PS::saveToFile.saveTimeout - File Save Timeout {#section-d22afd8ad86144b28684ed95a59db40e}

Valeur par défaut du délai d’expiration pour `req=saveToFile` les cas où `timeout=`n’est pas spécifié. `msec`. Une erreur est renvoyée si l&#39;opération d&#39;enregistrement n&#39;est pas terminée dans le délai imparti.
