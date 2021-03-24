---
description: La diffusion d’images fournit un préprocesseur de requête simple basé sur des règles de correspondance et de substitution d’expressions régulières.
solution: Experience Manager
title: Prétraitement des demandes
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# Prétraitement de la demande{#request-preprocessing}

La diffusion d’images fournit un préprocesseur de requête simple basé sur des règles de correspondance et de substitution d’expressions régulières.

Les collections de règles (jeux de règles) peuvent être jointes à chaque catalogue d’images, y compris le catalogue par défaut. Les règles sont spécifiées avec des fichiers au format XML.

Les règles de prétraitement des requêtes peuvent modifier les parties chemin et requête des requêtes avant d’être traitées par l’analyseur du serveur de plateformes, notamment en manipulant le chemin, en ajoutant des commandes, en modifiant les valeurs de commande et en appliquant des modèles ou des macros. Des règles peuvent également être utilisées pour configurer et remplacer certaines fonctions de sécurité qui sont normalement contrôlées uniquement avec des attributs de catalogue, comme l&#39;obscurcissement des requêtes, le marquage à l&#39;eau, ainsi que la limitation du service HTTP à des adresses IP client spécifiques.

Les règles de prétraitement des requêtes conviennent à diverses applications, dont certaines sont répertoriées ci-dessous :

* Mettez en oeuvre un mécanisme *chemins virtuels* qui permet de redéfinir le chemin de requête sur les chemins de fichier, FTP et HTTP.
* Application sélective de fonctions de sécurité, telles que le filigrane, filtrées par nom d’image ou chemin d’accès.
* L’absence de filigranes ou d’autres fonctions de sécurité lors de l’accès au serveur à partir d’adresses IP spécifiques.
* Forcer l’application de commandes, telles que `defaultImage=`, à toutes les requêtes ou aux requêtes présentant un modèle spécifique dans le chemin d’URL ou les chaînes de requête.
* Interdire l&#39;utilisation de commandes intensives en UC pour prévenir les abus de serveur.
* Autorisation de la localisation des images source sur les serveurs HTTP ou FTP tout en les spécifiant sur le chemin d’accès à la requête plutôt qu’avec `src=`.
* Contrôlez les paramètres de qualité d’image (tels que la qualité JPEG ou l’accentuation) en fonction du chemin d’accès à la demande ou du nom de l’image.

Vous trouverez des informations détaillées sur la création, l&#39;utilisation et la gestion des jeux de règles dans le [Guide de référence des jeux de règles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Voir aussi {#see-also}

[Référence](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e) du jeu de règles,  [attribut ::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
