---
description: Les références $var$ survenant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes.
solution: Experience Manager
title: Traitement variable dans les requêtes étrangères incorporées
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# Traitement variable dans les requêtes étrangères incorporées{#variable-processing-in-embedded-foreign-requests}

Les références $var$ survenant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes.

Cela permet de placer des requêtes étrangères incorporées dans un modèle dans un catalogue d’images.

En règle générale, les valeurs de variable devant être substituées dans des demandes étrangères doivent être codées en doublon, car aucun réencodage n’est appliqué avant que le serveur ne tente de transmettre l’URL étrangère finale.
