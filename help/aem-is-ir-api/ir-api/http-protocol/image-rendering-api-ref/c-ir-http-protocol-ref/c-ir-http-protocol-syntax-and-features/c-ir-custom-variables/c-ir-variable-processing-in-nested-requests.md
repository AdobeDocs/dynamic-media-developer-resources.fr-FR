---
title: Traitement des variables dans les requêtes imbriquées
description: Les références $var$ peuvent se trouver n’importe où dans les accolades d’une demande de rendu d’image ou de diffusion d’image imbriquée, y compris à gauche de "?" séparant le chemin de la requête.
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

Les références $var$ peuvent se trouver n’importe où dans les accolades d’une demande de rendu d’image ou de diffusion d’image imbriquée, y compris à gauche de &quot;?&quot; séparant le chemin de la requête.

Le serveur remplace ces références par des valeurs (provenant de l’URL ou de `catalog::Modifier` du catalogue d’images principal) avant d’analyser et de traiter davantage la requête imbriquée.

En outre, toutes les `$ *[!DNL var]*=` définitions provenant de l’URL et de `catalog::Modifier` sont transférées à toutes les requêtes Image Serving et Image Rendering imbriquées. Cela permet de s’assurer que toutes les définitions de variable sont disponibles pour tous les modèles, quel que soit le niveau d’imbrication.

Quel que soit le niveau d’imbrication, seul un codage HTTP à un seul passage doit être appliqué aux valeurs de variable qui doivent être remplacées n’importe où dans les demandes de rendu d’image ou de diffusion d’images imbriquées.
