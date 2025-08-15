---
description: La diffusion d’images fournit un préprocesseur de requête simple basé sur des règles de correspondance et de substitution d’expression régulière.
solution: Experience Manager
title: Prétraitement des demandes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Prétraitement des demandes{#request-preprocessing}

La diffusion d’images fournit un préprocesseur de requête simple basé sur des règles de correspondance et de substitution d’expression régulière.

Des collections de règles (ensembles de règles) peuvent être jointes à chaque catalogue d’images, y compris au catalogue par défaut. Les règles sont spécifiées avec des fichiers au format XML.

Les règles de prétraitement des requêtes peuvent modifier le chemin et les parties de requête des requêtes avant qu’elles ne soient traitées par l’analyseur du [!DNL Platform Server], notamment la manipulation du chemin, l’ajout de commandes, la modification des valeurs de commande et l’application de modèles ou de macros. Les règles peuvent également être utilisées pour configurer et remplacer certaines fonctionnalités de sécurité qui ne sont normalement contrôlées qu’avec des attributs de catalogue, tels que l’obscurcissement des requêtes, le filigrane, ainsi que pour limiter le service HTTP à des adresses IP clientes spécifiques.

Les règles de prétraitement des demandes conviennent à diverses applications, dont certaines sont répertoriées ci-dessous :

* Implémentez un mécanisme *chemins virtuels* qui permet de remapper le chemin d’accès de la requête aux chemins d’accès aux fichiers, FTP et HTTP.
* Application sélective des fonctionnalités de sécurité, telles que le filigrane, filtrées par nom ou chemin d’accès d’image.
* L’omission des filigranes ou d’autres fonctionnalités de sécurité lors de l’accès au serveur à partir d’adresses IP spécifiques.
* Application forcée de commandes, telles que `defaultImage=`, à toutes les requêtes ou aux requêtes qui présentent un modèle spécifique dans le chemin d’accès à l’URL ou les chaînes de requête.
* Interdiction d’utiliser des commandes à utilisation intensive de CPU pour empêcher les abus de serveur.
* Autoriser la localisation des images sources sur des serveurs HTTP ou FTP tout en les spécifiant sur le chemin d’accès de la requête plutôt qu’avec `src=`.
* Contrôlez les paramètres de qualité d’image (tels que la qualité de JPEG ou l’accentuation) en fonction du chemin d’accès de la requête ou du nom de l’image.

Vous trouverez des informations détaillées sur la création, l’utilisation et la gestion des ensembles de règles dans la [Référence des ensembles de règles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Voir aussi {#see-also}

[Référence du jeu de règles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [attribute::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
