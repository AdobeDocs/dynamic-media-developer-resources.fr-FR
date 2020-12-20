---
description: Le rendu d’image fournit un préprocesseur de demande simple basé sur des règles de correspondance et de substitution d’expressions régulières.
seo-description: Le rendu d’image fournit un préprocesseur de demande simple basé sur des règles de correspondance et de substitution d’expressions régulières.
seo-title: Prétraitement de la demande *
solution: Experience Manager
title: Prétraitement de la demande *
topic: Scene7 Image Serving - Image Rendering API
uuid: ef69ea23-753c-40c8-9edd-eab9c8820c98
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Prétraitement de la demande *{#request-pre-processing}

Le rendu d’image fournit un préprocesseur de demande simple basé sur des règles de correspondance et de substitution d’expressions régulières.

Les collections de règles (jeux de règles) peuvent être jointes à chaque catalogue de matières, y compris le catalogue par défaut. Les règles sont spécifiées avec des fichiers au format XML.

Les règles de prétraitement des requêtes peuvent modifier les parties de chemin et de requête des requêtes avant d’être traitées par l’analyseur de rendu d’image, notamment en manipulant le chemin, en ajoutant des commandes, en modifiant les valeurs de commande et en appliquant des modèles ou des macros. Les règles peuvent également être utilisées pour configurer et remplacer certaines fonctionnalités qui sont normalement contrôlées uniquement avec des attributs de catalogue, comme la définition de la taille d’image de réponse par défaut ou la limitation du service HTTP à des adresses IP client spécifiques.

Les règles de prétraitement des demandes conviennent à diverses applications, dont certaines sont énumérées ci-dessous :

* Mettez en oeuvre un mécanisme *chemins virtuels* qui permet de redéfinir le chemin de requête sur les chemins de fichier, FTP et HTTP.
* Interdire l&#39;utilisation de commandes gourmandes en CPU pour éviter les abus de serveur.
* Contrôlez les paramètres de qualité d’image (tels que la qualité JPEG ou l’accentuation) en fonction du chemin d’accès à la demande ou du nom de l’image.

Vous trouverez des informations détaillées sur la création, l&#39;utilisation et la gestion des jeux de règles dans la Référence du jeu de règles.

Voir aussi Référence du jeu de règles, attribut ::RuleSetFile
