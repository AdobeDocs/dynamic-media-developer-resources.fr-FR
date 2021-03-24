---
description: Les références $var$ peuvent se trouver n’importe où à l’intérieur des accolades d’une demande de diffusion d’images ou de rendu d’image imbriquée, y compris à gauche de l’"?" séparant le chemin de la requête.
solution: Experience Manager
title: Traitement des variables dans les requêtes imbriquées
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# Traitement des variables dans les requêtes imbriquées{#variable-processing-in-nested-requests}

Les références $var$ peuvent se trouver n’importe où à l’intérieur des accolades d’une demande de diffusion d’images ou de rendu d’image imbriquée, y compris à gauche de l’&quot;?&quot; séparant le chemin de la requête.

Le serveur remplace ces références par des valeurs (provenant de l’URL ou de `catalog::Modifier` du catalogue d’images principal) avant d’analyser et de traiter davantage la demande imbriquée.

En outre, toutes les définitions `$ *[!DNL var]*=` de l’URL et `catalog::Modifier` sont transférées à toutes les demandes de diffusion d’images et de rendu d’image imbriquées. Ainsi, toutes les définitions de variable sont disponibles pour tous les modèles, quel que soit le niveau d’imbrication.

Quel que soit le niveau d’imbrication, seul le codage HTTP à une seule passe doit être appliqué aux valeurs de variable qui doivent être remplacées n’importe où dans les demandes de rendu d’image ou de diffusion d’image imbriquées.
