---
description: Les références $var$ se trouvant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes.
solution: Experience Manager
title: Traitement variable dans les requêtes étrangères incorporées
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Traitement variable dans les requêtes étrangères incorporées{#variable-processing-in-embedded-foreign-requests}

Les références $var$ se trouvant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes.

Cela permet de placer des requêtes étrangères incorporées dans un modèle dans un catalogue d’images.

Les valeurs de variable qui doivent être remplacées par des requêtes étrangères doivent généralement être codées en double encodage, car aucun réencodage n’est appliqué avant que le serveur ne tente de transmettre l’URL étrangère finale.
