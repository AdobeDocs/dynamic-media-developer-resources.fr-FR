---
title: Traitement des variables dans les requêtes imbriquées
description: $var$ références peuvent apparaître n’importe où entre les accolades d’une requête imbriquée de service d’image ou de rendu d’image, y compris à gauche du caractère « ? ». séparant le chemin de la requête.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Traitement des variables dans les requêtes imbriquées{#variable-processing-in-nested-requests}

$var$ références peuvent apparaître n’importe où entre les accolades d’une requête imbriquée de service d’image ou de rendu d’image, y compris à gauche du caractère « ? ». séparant le chemin de la requête.

Le serveur remplace ces références par des valeurs (provenant de l’URL ou du `catalog::Modifier` catalogue d’images principal) avant d’analyser et de traiter la demande imbriquée.

En outre, toutes les `$ *[!DNL var]*=` définitions de l’URL et `catalog::Modifier` sont transférées à toutes les demandes imbriquées de serveur d’image et de rendu d’image. Cela garantit que toutes les définitions de variables sont disponibles pour tous les modèles, quel que soit le niveau d’imbrication.

Quel que soit le niveau d’imbrication, seul le codage HTTP monopassage doit être appliqué aux valeurs de variable qui doivent être substituées n’importe où dans les requêtes imbriquées de rendu d’image ou de diffusion d’images.
