---
title: Pré-traitement des demandes
description: Le rendu d’image fournit un préprocesseur de requête simple basé sur des règles de correspondance et de substitution d’expression régulière.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
TQID: 'https://experienceleague.adobe.com/zs4izZzuO7u6wYOPmdd8AT7r4q-cUFXWUlB1MW6aV0Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 0%

---

# Pré-traitement des demandes{#request-pre-processing}

Le rendu d’image fournit un préprocesseur de requête simple basé sur des règles de correspondance et de substitution d’expression régulière.

Des collections de règles (ensembles de règles) peuvent être associées à chaque catalogue de matières, y compris le catalogue par défaut. Les règles sont spécifiées avec des fichiers au format XML.

Les règles de pré-traitement des requêtes peuvent modifier le chemin et les parties de requête des requêtes avant qu’elles ne soient traitées par l’analyseur de rendu d’image. Ce précepte comprend la manipulation du chemin d’accès, l’ajout de commandes, la modification des valeurs de commande et l’application de modèles ou de macros. Les règles peuvent également être utilisées pour configurer et remplacer certaines fonctionnalités qui ne sont normalement contrôlées qu’avec des attributs de catalogue, telles que la définition de la taille de l’image de réponse par défaut ou la limitation du service HTTP à des adresses IP clientes spécifiques.

Les règles de prétraitement des demandes conviennent à diverses applications, dont certaines sont répertoriées ci-dessous :

* Implémentez un mécanisme *chemins virtuels* qui permet de remapper le chemin d’accès de la requête aux chemins d’accès aux fichiers, FTP et HTTP.
* Interdiction d’utiliser des commandes à utilisation intensive de CPU pour empêcher les abus de serveur.
* Contrôlez les paramètres de qualité d’image (tels que la qualité de JPEG ou l’accentuation) en fonction du chemin d’accès de la requête ou du nom de l’image.

Vous trouverez des informations détaillées sur la création, l’utilisation et la gestion des ensembles de règles dans la référence des ensembles de règles.

Voir aussi Référence de l’ensemble de règles, attribute::RuleSetFile

