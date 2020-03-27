---
description: Paramètres généraux du serveur
seo-description: Paramètres généraux du serveur
seo-title: Généraux
solution: Experience Manager
title: Généraux
topic: Scene7 Image Serving - Image Rendering API
uuid: d7ec3dba-64b8-431b-b446-84ab6139ba8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Généraux{#general}

Paramètres généraux du serveur

## TC::PsPort - Port D’Écoute Principal {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Spécifie le port d’écoute principal pour le serveur de plateformes. Ce port permet également d’accéder à la documentation et aux exemples de pages pour la diffusion d’images, le rendu d’images et les visionneuses Scene7 (si elles sont installées).

## IS::CacheServerUrl - Url Racine Du Service De Mise En Cache {#section-bcca227a1f91453b834db4ea050968e2}

Spécifie le chemin d’accès racine HTTP permettant au serveur d’images d’accéder au service de mise en cache. Doit être défini sur [!DNL http://localhost:TC::PsPort /is/cache/secondary], avec le numéro de port correspondant `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - TTL par défaut de la source d&#39;image distante {#section-e4c31228b459492cacd2f482d9575f71}

TTL pour les images mises en cache obtenues via HTTP à partir d’une source distante à l’aide du `src={…}` concept. Utilisé uniquement lorsque le serveur distant n’inclut pas d’en-tête Expiration dans sa réponse HTTP. Valeur entière en secondes.

## IS::RemoteUrlTimeout - Délai d’expiration de la source d’image distante {#section-437646c479cc4bea81dae42100a3c50a}

Heure à laquelle le serveur d’images attend qu’un serveur distant diffuse le fichier image demandé via HTTP avant de renvoyer une erreur. Valeur entière en secondes.

## PS::allowDefaultCatalogRequests - Activer/désactiver les requêtes de catalogue par défaut {#section-484e442a115a49b4ac269d1718b351e1}

Définissez cette variable sur false pour interdire les requêtes qui n’incluent pas d’ID de catalogue valide dans le chemin d’accès. Default is `true`. Lorsqu’elle est définie sur `false`, une erreur est renvoyée pour les requêtes sans ID de catalogue.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>`req=catalogprops` n’est pas soumise à ce paramètre.

## PS::saveToFile.saveTimeout - Délai d’expiration de l’enregistrement du fichier {#section-d22afd8ad86144b28684ed95a59db40e}

Valeur du délai d’expiration par défaut pour `req=saveToFile` les cas `timeout=`non spécifiés. `msec`. Une erreur est renvoyée si l&#39;opération d&#39;enregistrement n&#39;est pas terminée dans le délai spécifié.
