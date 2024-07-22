---
description: La diffusion d’images fournit un préprocesseur de requêtes simple basé sur les règles de correspondance et de substitution des expressions régulières.
solution: Experience Manager
title: Prétraitement des requêtes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Prétraitement des requêtes{#request-preprocessing}

La diffusion d’images fournit un préprocesseur de requêtes simple basé sur les règles de correspondance et de substitution des expressions régulières.

Des collections de règles (ensembles de règles) peuvent être jointes à chaque catalogue d’images, y compris le catalogue par défaut. Les règles sont spécifiées avec des fichiers au format XML.

Les règles de prétraitement des requêtes peuvent modifier les parties de chemin et de requête des requêtes avant qu’elles ne soient traitées par l’analyseur de [!DNL Platform Server], y compris la manipulation du chemin, l’ajout de commandes, la modification des valeurs de commande et l’application de modèles ou de macros. Des règles peuvent également être utilisées pour configurer et remplacer certaines fonctionnalités de sécurité qui sont normalement contrôlées uniquement avec des attributs de catalogue, comme l’obscurcissement des requêtes, le marquage à l’eau, ainsi que la limitation du service HTTP à des adresses IP client spécifiques.

Les règles de prétraitement des requêtes conviennent à diverses applications, dont certaines sont répertoriées ci-dessous :

* Implémentez un mécanisme *virtual paths* qui permet de mapper à nouveau le chemin de requête sur les chemins de fichier, FTP et HTTP.
* Application sélective de fonctionnalités de sécurité, telles que le filigrane, filtrées par nom ou chemin d’accès de l’image.
* Omission de filigranes ou autres fonctions de sécurité lors de l’accès au serveur à partir d’adresses IP spécifiques.
* Forcer l’application de commandes, telles que `defaultImage=`, à toutes les requêtes ou aux requêtes présentant un modèle spécifique dans le chemin d’URL ou les chaînes de requête.
* Interdire l’utilisation de commandes intensives en processeur pour éviter les abus de serveur.
* Autorisation de l’emplacement des images source sur les serveurs HTTP ou FTP tout en les spécifiant sur le chemin de la requête plutôt qu’avec `src=`.
* Contrôlez les paramètres de qualité de l’image (tels que la qualité ou l’accentuation du JPEG) en fonction du chemin d’accès à la requête ou du nom de l’image.

Vous trouverez des informations détaillées sur la création, l’utilisation et la gestion des ensembles de règles dans la [référence du jeu de règles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Voir aussi {#see-also}

[Référence du jeu de règles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [attribute::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
