---
title: Traitement des variables dans les requêtes étrangères incorporées
description: $var références $ apparaissant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par les valeurs de définition de variable correspondantes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Traitement des variables dans les requêtes étrangères incorporées{#variable-processing-in-embedded-foreign-requests}

Toutes les `$var$` références qui apparaissent n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par les valeurs de définition de variable correspondantes.

Permet de placer des requêtes étrangères incorporées dans un modèle d’un catalogue d’images.

Les valeurs de variable qui doivent être substituées dans des requêtes étrangères doivent généralement être codées deux fois, car aucun récodage n’est appliqué avant que le serveur ne tente de transmettre l’URL étrangère finale.
