---
description: Les références $var$ survenant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes.
seo-description: Les références $var$ survenant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes.
seo-title: Traitement variable dans les requêtes étrangères incorporées
solution: Experience Manager
title: Traitement variable dans les requêtes étrangères incorporées
uuid: b4334a2e-dab1-4458-ab3d-bb79d2c4fdd4
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# Traitement variable dans les requêtes étrangères incorporées{#variable-processing-in-embedded-foreign-requests}

Les références $var$ survenant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes.

Cela permet de placer des requêtes étrangères incorporées dans un modèle dans un catalogue d’images.

En règle générale, les valeurs de variable devant être substituées dans des demandes étrangères doivent être codées en doublon, car aucun réencodage n’est appliqué avant que le serveur ne tente de transmettre l’URL étrangère finale.
