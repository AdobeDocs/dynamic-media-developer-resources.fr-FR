---
title: Pré-traitement d’une demande
description: Image Rendering fournit un préprocesseur de requête simple basé sur des règles de correspondance et de substitution d’expressions régulières.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 20f4922402bd31c71ae650a01597b574220809fa
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Pré-traitement d’une demande{#request-pre-processing}

Image Rendering fournit un préprocesseur de requête simple basé sur des règles de correspondance et de substitution d’expressions régulières.

Des collections de règles (ensembles de règles) peuvent être attachées à chaque catalogue de matériaux, y compris le catalogue par défaut. Les règles sont spécifiées avec des fichiers au format XML.

Les règles de prétraitement des demandes peuvent modifier les parties chemin et requête des requêtes avant qu’elles ne soient traitées par l’analyseur Image Rendering. Ce précepte inclut la manipulation du chemin d’accès, l’ajout de commandes, la modification des valeurs de commande et l’application de modèles ou de macros. Les règles peuvent également être utilisées pour configurer et remplacer certaines fonctionnalités qui ne sont normalement contrôlées qu’avec des attributs de catalogue, telles que la définition de la taille d’image de réponse par défaut ou la limitation du service HTTP à des adresses IP client spécifiques.

Les règles de prétraitement des requêtes conviennent à diverses applications, dont certaines sont répertoriées ci-dessous :

* Implémentez un *mécanisme de chemins* virtuels, qui permet de remapper le chemin d’accès de la demande aux chemins d’accès au fichier, FTP et HTTP.
* Interdiction de l’utilisation de commandes gourmandes en ressources CPU pour éviter toute utilisation abusive du serveur.
* Contrôlez les paramètres de qualité d’image (tels que la qualité JPEG ou l’accentuation) en fonction du chemin d’accès ou du nom de l’image de la demande.

Vous trouverez des informations détaillées sur la création, l’utilisation et la gestion des ensembles de règles dans la Référence des ensembles de règles.

Voir aussi Référence d’ensemble de règles, attribut ::RuleSetFile
