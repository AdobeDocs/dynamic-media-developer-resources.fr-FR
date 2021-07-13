---
description: Le serveur surveille en permanence le dossier du catalogue et recharge automatiquement un catalogue d’images, y compris les fichiers de données de catalogue associés, lorsqu’il détecte que le fichier d’attribut du catalogue principal a été modifié.
solution: Experience Manager
title: Mise à jour des catalogues d’images
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: b520b4f3-6717-4768-99e2-78a76d1ede24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# Mise à jour des catalogues d’images{#updating-image-catalogs}

Le serveur surveille en permanence le dossier du catalogue et recharge automatiquement un catalogue d’images, y compris les fichiers de données de catalogue associés, lorsqu’il détecte que le fichier d’attribut du catalogue principal a été modifié.

Pour mettre à jour les catalogues d’images sur le serveur, vous devez d’abord remplacer tous les fichiers de données de catalogue qui doivent être modifiés, puis remplacer (ou &quot;toucher&quot; pour mettre à jour la date du fichier) le fichier d’attributs de catalogue pour déclencher le rechargement du catalogue.

## Mises à jour incrémentielles {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

Le chargement et le traitement de catalogues d’images volumineuses peuvent placer une charge importante sur le serveur et peut avoir un impact négatif sur les opérations de diffusion en direct. Pour minimiser cet impact, il est recommandé de mettre en oeuvre un mécanisme de mise à jour incrémentielle du catalogue, qui fonctionne comme suit :

Un Principal fichier catalogue contenant toutes les images est chargé de nuit pendant les heures de faible trafic. S’il est nécessaire, au cours de la journée, d’ajouter ou de modifier des enregistrements dans le catalogue d’images, un autre fichier de données image est créé, contenant uniquement les enregistrements nouveaux ou modifiés. Ce fichier est enregistré en tant que fichier de données image secondaire dans `attribute::CatalogFile`. Le serveur détecte que le fichier d’attributs du catalogue a changé, puis vérifie les fichiers de données du catalogue qui ont changé. Si le fichier de données image principal n’a pas été modifié, le serveur charge ou recharge uniquement le fichier de données incrémentiel. Comme ce fichier est généralement beaucoup plus petit que le fichier de catalogue principal, l’impact sur le serveur est beaucoup plus réduit par rapport au rechargement du catalogue principal.

Les mises à jour incrémentielles peuvent réduire considérablement l’impact sur le serveur lors d’un trafic important. Il est recommandé de fusionner régulièrement le fichier de données de catalogue incrémentiel dans le fichier de données de catalogue principal pendant les heures à faible trafic afin de maintenir des performances optimales du serveur.
