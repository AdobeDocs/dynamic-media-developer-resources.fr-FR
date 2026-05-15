---
description: Paramètres généraux du serveur
solution: Experience Manager
title: Généraux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
TQID: 'https://experienceleague.adobe.com/hjww7EYpf4xNxpUFQ1fudMOqNtokgykthwhonn78ZFE'
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
source-wordcount: 227
ht-degree: 0%

---

# Généraux{#general}

Paramètres généraux du serveur

## TC::PsPort - Port d&#39;écoute principal {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Spécifie le port d&#39;écoute principal pour le [!DNL Platform Server]. Ce port est également utilisé pour accéder à la documentation et aux pages d’exemple pour la diffusion d’images, le rendu d’images et les visionneuses Dynamic Media (si elles sont installées).

## IS::CacheServerUrl - URL racine du service de mise en cache {#section-bcca227a1f91453b834db4ea050968e2}

Indique le chemin d’accès racine HTTP pour autoriser le serveur d’images à accéder au service de mise en cache. Doit être défini sur [!DNL http://localhost:TC::PsPort /is/cache/secondary], avec le numéro de port correspondant à `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - TTL par défaut Image Source à distance {#section-e4c31228b459492cacd2f482d9575f71}

TTL pour les images mises en cache obtenues par le biais du protocole HTTP à partir d’une source distante à l’aide du concept `src={…}`. Utilisé uniquement lorsque le serveur distant n’inclut pas d’en-tête Expiration dans sa réponse HTTP. Valeur entière en secondes.

## IS::RemoteUrlTimeout - Délai d’expiration d’Image Source distant {#section-437646c479cc4bea81dae42100a3c50a}

Temps pendant lequel le serveur d’images attend qu’un serveur distant lui fournisse le fichier image demandé par le biais du protocole HTTP avant de renvoyer une erreur. Valeur entière en secondes.

## PS::allowDefaultCatalogRequests - Active/Désactive les demandes de catalogue par défaut {#section-484e442a115a49b4ac269d1718b351e1}

Définissez cette variable sur false pour interdire les requêtes qui n’incluent pas d’ID de catalogue valide dans le chemin d’accès. La valeur par défaut est `true`. Lorsque la valeur est définie sur `false`, une erreur est renvoyée pour les requêtes sans ID de catalogue.

>[!NOTE]
>
>`req=catalogprops` n’est pas soumis à ce paramètre.

## PS::saveToFile.saveTimeout - Délai d&#39;expiration de l&#39;enregistrement du fichier {#section-d22afd8ad86144b28684ed95a59db40e}

Valeur de délai d’expiration par défaut pour `req=saveToFile` lorsque `timeout=` n’est pas spécifié. `msec`. Une erreur est renvoyée si l’opération d’enregistrement n’est pas terminée dans le délai spécifié.
