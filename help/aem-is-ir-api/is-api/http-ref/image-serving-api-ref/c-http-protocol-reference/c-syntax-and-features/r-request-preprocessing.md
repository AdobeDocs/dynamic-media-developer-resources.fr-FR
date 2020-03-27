---
description: La diffusion d’images fournit un préprocesseur de requête simple basé sur les règles de correspondance et de substitution des   régulières.
seo-description: La diffusion d’images fournit un préprocesseur de requête simple basé sur les règles de correspondance et de substitution des   régulières.
seo-title: Prétraitement des demandes
solution: Experience Manager
title: Prétraitement des demandes
topic: Scene7 Image Serving - Image Rendering API
uuid: 375bbca2-7a4a-49a9-9577-86e6b2f19990
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prétraitement des demandes{#request-preprocessing}

La diffusion d’images fournit un préprocesseur de requête simple basé sur les règles de correspondance et de substitution des   régulières.

Les collections de règles (jeux de règles) peuvent être jointes à chaque catalogue d’images, y compris le catalogue par défaut. Les règles sont spécifiées avec des fichiers au format XML.

Les règles de prétraitement des requêtes peuvent modifier le chemin et  parties de requêtes avant d’être traitées par l’analyseur du serveur de plateformes, y compris la manipulation du chemin, l’ajout de commandes, la modification des valeurs de commande et l’application de modèles ou de macros. Des règles peuvent également être utilisées pour configurer et remplacer certaines fonctionnalités de sécurité qui sont normalement contrôlées uniquement avec des attributs de catalogue, tels que l’obscurcissement de requête, le marquage à l’eau, ainsi que la limitation du service HTTP à des adresses IP client spécifiques.

Les règles de prétraitement des demandes sont adaptées à diverses applications, dont certaines sont répertoriées ci-dessous :

* Mettez en oeuvre un mécanisme de chemins ** virtuels qui permet de redéfinir le chemin de requête vers les chemins de fichier, FTP et HTTP.
* Applique de manière sélective des fonctions de sécurité, telles que le filigrane, filtrées par nom d’image ou chemin d’accès.
* L’absence de filigranes ou d’autres fonctions de sécurité lors de l’accès au serveur à partir d’adresses IP spécifiques.
* Obligation d’appliquer des commandes, telles que `defaultImage=`à toutes les requêtes ou aux requêtes qui présentent un modèle spécifique dans le chemin d’accès à l’URL ou les chaînes de  du.
* Interdire l&#39;utilisation de commandes intensives en UC pour prévenir les abus de serveur.
* Autoriser l’emplacement des images source sur les serveurs HTTP ou FTP tout en les spécifiant sur le chemin de requête plutôt qu’avec `src=`.
* Contrôlez les paramètres de qualité de l’image (tels que la qualité JPEG ou l’accentuation) en fonction du chemin de demande ou du nom de l’image.

Vous trouverez des informations détaillées sur la création, l’utilisation et la gestion des jeux de règles dans le Guide de référence [des jeux de](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)règles.

## Voir aussi {#see-also}

[Référence](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)du jeu de règles, [attribut::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
