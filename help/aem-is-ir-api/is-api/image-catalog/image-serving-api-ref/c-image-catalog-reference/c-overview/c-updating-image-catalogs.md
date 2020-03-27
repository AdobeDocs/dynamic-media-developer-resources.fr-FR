---
description: Le serveur surveille en permanence le dossier du catalogue et recharge automatiquement un catalogue d’images, y compris les fichiers de données de catalogue associés, lorsqu’il détecte que le fichier d’attribut de catalogue principal a été modifié.
seo-description: Le serveur surveille en permanence le dossier du catalogue et recharge automatiquement un catalogue d’images, y compris les fichiers de données de catalogue associés, lorsqu’il détecte que le fichier d’attribut de catalogue principal a été modifié.
seo-title: Mise à jour des catalogues d’images
solution: Experience Manager
title: Mise à jour des catalogues d’images
topic: Scene7 Image Serving - Image Rendering API
uuid: 7e2557c4-1155-429b-a630-a2aff6725a3b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Mise à jour des catalogues d’images{#updating-image-catalogs}

Le serveur surveille en permanence le dossier du catalogue et recharge automatiquement un catalogue d’images, y compris les fichiers de données de catalogue associés, lorsqu’il détecte que le fichier d’attribut de catalogue principal a été modifié.

Pour mettre à jour les catalogues d’images sur le serveur, remplacez d’abord tous les fichiers de données de catalogue qui doivent être modifiés, puis remplacez (ou &quot;tactile&quot; pour mettre à jour la date du fichier) le fichier d’attributs du catalogue afin de déclencher le rechargement du catalogue.

## Mises à jour incrémentielles {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

Le chargement et le traitement des catalogues d’images volumineuses peuvent placer une charge importante sur le serveur et avoir un impact négatif sur les opérations de diffusion en direct. Pour minimiser cet impact, il est recommandé de mettre en oeuvre un mécanisme de mise à jour incrémentielle du catalogue, qui fonctionne comme suit :

Un fichier catalogue principal contenant toutes les images est chargé de nuit pendant les heures de faible trafic. S’il est nécessaire durant la journée d’ajouter ou de modifier des enregistrements dans le catalogue d’images, un autre fichier de données image est créé, qui ne contient que les enregistrements nouveaux ou modifiés. Ce fichier est enregistré en tant que fichier de données image secondaire dans `attribute::CatalogFile`. Le serveur détecte que le fichier d’attribut de catalogue a changé, puis vérifie quels fichiers de données de catalogue ont changé. Si le fichier de données image principal n’a pas été modifié, le serveur charge ou recharge uniquement le fichier de données incrémentielles. Comme ce fichier est généralement beaucoup plus petit que le fichier catalogue principal, l’impact sur le serveur est beaucoup moins important que le rechargement du catalogue principal.

Des mises à jour incrémentielles peuvent réduire considérablement l’impact sur le serveur lors d’un trafic important. Il est recommandé de fusionner régulièrement le fichier de données de catalogue incrémentielles dans le fichier de données de catalogue principal pendant les heures de faible trafic afin de préserver les performances optimales du serveur.
