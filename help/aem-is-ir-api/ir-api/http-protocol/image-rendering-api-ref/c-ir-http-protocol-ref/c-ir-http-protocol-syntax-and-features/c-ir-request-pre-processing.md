---
description: Le rendu d’image fournit un préprocesseur de requête simple basé sur les règles de correspondance et de substitution des   régulières.
seo-description: Le rendu d’image fournit un préprocesseur de requête simple basé sur les règles de correspondance et de substitution des   régulières.
seo-title: Prétraitement des demandes *
solution: Experience Manager
title: Prétraitement des demandes *
topic: Scene7 Image Serving - Image Rendering API
uuid: ef69ea23-753c-40c8-9edd-eab9c8820c98
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prétraitement des demandes *{#request-pre-processing}

Le rendu d’image fournit un préprocesseur de requête simple basé sur les règles de correspondance et de substitution des   régulières.

Des collections de règles (jeux de règles) peuvent être jointes à chaque catalogue de matières, y compris le catalogue par défaut. Les règles sont spécifiées avec des fichiers au format XML.

Les règles de prétraitement des requêtes peuvent modifier le chemin et  parties de requêtes avant d’être traitées par l’analyseur de rendu d’image, y compris la manipulation du chemin, l’ajout de commandes, la modification des valeurs de commande et l’application de modèles ou de macros. Vous pouvez également utiliser des règles pour configurer et remplacer certaines fonctionnalités qui sont normalement contrôlées uniquement avec des attributs de catalogue, comme la définition de la taille d’image de réponse par défaut ou la limitation du service HTTP à des adresses IP client spécifiques.

Les règles de prétraitement des demandes sont adaptées à diverses applications, dont certaines sont répertoriées ci-dessous :

* Mettez en oeuvre un mécanisme de chemins ** virtuels qui permet de redéfinir le chemin de requête vers les chemins de fichier, FTP et HTTP.
* Interdire l&#39;utilisation de commandes gourmandes en ressources processeur pour éviter les abus de serveur.
* Contrôlez les paramètres de qualité de l’image (tels que la qualité JPEG ou l’accentuation) en fonction du chemin de demande ou du nom de l’image.

Vous trouverez des informations détaillées sur la création, l’utilisation et la gestion des jeux de règles dans le Guide de référence des jeux de règles.

Voir aussi Référence du jeu de règles, attribut::RuleSetFile
