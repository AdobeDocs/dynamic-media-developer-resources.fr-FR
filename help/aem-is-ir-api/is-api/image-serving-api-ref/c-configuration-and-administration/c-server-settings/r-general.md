---
description: Paramètres généraux du serveur
solution: Experience Manager
title: Généraux
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---


# Généraux{#general}

Paramètres généraux du serveur

## TC::PsPort - Port d&#39;écoute principal {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Spécifie le port d’écoute principal pour le serveur de plateformes. Ce port permet également d’accéder à la documentation et aux exemples de pages pour la diffusion d’images, le rendu d’images et les visionneuses Dynamic Media (si elles sont installées).

## IS::CacheServerUrl - URL racine du service de mise en cache {#section-bcca227a1f91453b834db4ea050968e2}

Spécifie le chemin d’accès racine HTTP pour permettre à Image Server d’accéder au service de mise en cache. Doit être défini sur [!DNL http://localhost:TC::PsPort /is/cache/secondary], avec le numéro de port correspondant à `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - TTL par défaut de la source d&#39;image distante {#section-e4c31228b459492cacd2f482d9575f71}

TTL pour les images mises en cache obtenues via HTTP à partir d’une source distante à l’aide de la construction `src={…}`. Utilisé uniquement lorsque le serveur distant n’inclut pas d’en-tête Expiration dans sa réponse HTTP. Valeur entière en secondes.

## IS::RemoteUrlTimeout - Délai d&#39;expiration de la source d&#39;image distante {#section-437646c479cc4bea81dae42100a3c50a}

Heure à laquelle le serveur d’images attend qu’un serveur distant diffuse le fichier image demandé via HTTP avant de renvoyer une erreur. Valeur entière en secondes.

## PS::allowDefaultCatalogRequests - Activer/désactiver les requêtes de catalogue par défaut {#section-484e442a115a49b4ac269d1718b351e1}

Définissez cette variable sur false pour interdire les requêtes qui n’incluent pas d’ID de catalogue valide dans le chemin d’accès. La valeur par défaut est `true`. Lorsqu’elle est définie sur `false`, une erreur est renvoyée pour les requêtes sans ID de catalogue.

>[!NOTE]
>
>`req=catalogprops` n’est pas soumis à ce paramètre.

## PS::saveToFile.saveTimeout - File Save Timeout {#section-d22afd8ad86144b28684ed95a59db40e}

Valeur de délai d’expiration par défaut pour `req=saveToFile` lorsque `timeout=`n’est pas spécifié. `msec`. Une erreur est renvoyée si l&#39;opération d&#39;enregistrement n&#39;est pas terminée dans le délai imparti.
