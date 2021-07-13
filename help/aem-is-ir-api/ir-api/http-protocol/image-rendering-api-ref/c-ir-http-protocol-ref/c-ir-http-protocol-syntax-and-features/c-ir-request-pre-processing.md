---
description: Le rendu d’image fournit un préprocesseur de requêtes simple basé sur les règles de correspondance et de substitution des expressions régulières.
solution: Experience Manager
title: Prétraitement des demandes *
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# Prétraitement des demandes *{#request-pre-processing}

Le rendu d’image fournit un préprocesseur de requêtes simple basé sur les règles de correspondance et de substitution des expressions régulières.

Des collections de règles (ensembles de règles) peuvent être jointes à chaque catalogue de matières, y compris le catalogue par défaut. Les règles sont spécifiées avec des fichiers au format XML.

Les règles de prétraitement des requêtes peuvent modifier les parties de chemin et de requête des requêtes avant qu’elles ne soient traitées par l’analyseur de rendu d’image, notamment en manipulant le chemin, en ajoutant des commandes, en modifiant les valeurs de commande et en appliquant des modèles ou des macros. Des règles peuvent également être utilisées pour configurer et remplacer certaines fonctionnalités normalement contrôlées uniquement avec des attributs de catalogue, comme la définition de la taille de l’image de réponse par défaut ou la limitation du service HTTP à des adresses IP client spécifiques.

Les règles de prétraitement des demandes sont adaptées à diverses applications, dont certaines sont répertoriées ci-dessous :

* Implémentez un mécanisme *virtual paths* qui permet de mapper à nouveau le chemin de requête sur les chemins de fichier, FTP et HTTP.
* Interdire l’utilisation de commandes intensives en processeur pour éviter les abus de serveur.
* Contrôlez les paramètres de qualité de l’image (tels que la qualité JPEG ou l’accentuation) en fonction du chemin d’accès à la requête ou du nom de l’image.

Vous trouverez des informations détaillées sur la création, l’utilisation et la gestion des jeux de règles dans la référence du jeu de règles.

Voir aussi Référence du jeu de règles, attribut::RuleSetFile
