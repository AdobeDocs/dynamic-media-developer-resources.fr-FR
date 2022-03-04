---
description: Paramètres généraux du serveur
solution: Experience Manager
title: Généraux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Généraux{#general}

Paramètres généraux du serveur

## TC::PsPort - Port D’Écoute Principal {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Spécifie le port d’écoute principal du serveur Platform. Ce port est également utilisé pour accéder à la documentation et aux exemples de pages pour le serveur d’images, le rendu d’images et les visionneuses Dynamic Media (le cas échéant).

## IS::CacheServerUrl - Url Racine Du Service De Mise En Cache {#section-bcca227a1f91453b834db4ea050968e2}

Spécifie le chemin d’accès racine HTTP pour autoriser le serveur d’images à accéder au service de mise en cache. Doit être défini sur [!DNL http://localhost:TC::PsPort /is/cache/secondary], avec le numéro de port correspondant `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - Remote Image Source Default TTL {#section-e4c31228b459492cacd2f482d9575f71}

TTL pour les images mises en cache obtenues via HTTP à partir d’une source distante à l’aide de la fonction `src={…}` construire. Utilisée uniquement lorsque le serveur distant n’inclut pas d’en-tête Expiration dans sa réponse HTTP. Valeur entière en secondes.

## IS::RemoteUrlTimeout - Remote Image Source Timeout {#section-437646c479cc4bea81dae42100a3c50a}

Heure pendant laquelle le serveur d’images attend qu’un serveur distant diffuse le fichier image demandé via HTTP avant de renvoyer une erreur. Valeur entière en secondes.

## PS::allowDefaultCatalogRequests - Activer/Désactiver les requêtes de catalogue par défaut {#section-484e442a115a49b4ac269d1718b351e1}

Définissez cette variable sur false pour interdire les requêtes qui n’incluent pas d’identifiant de catalogue valide dans le chemin d’accès. La valeur par défaut est `true`. Lorsque la variable est définie sur `false`, une erreur est renvoyée pour les requêtes sans identifiant de catalogue.

>[!NOTE]
>
>`req=catalogprops` n’est pas soumis à ce paramètre.

## PS::saveToFile.saveTimeout - File Save Timeout {#section-d22afd8ad86144b28684ed95a59db40e}

Valeur par défaut du délai d’expiration pour `req=saveToFile` when `timeout=`n’est pas spécifié. `msec`. Une erreur est renvoyée si l’opération de sauvegarde n’est pas terminée dans le délai spécifié.
