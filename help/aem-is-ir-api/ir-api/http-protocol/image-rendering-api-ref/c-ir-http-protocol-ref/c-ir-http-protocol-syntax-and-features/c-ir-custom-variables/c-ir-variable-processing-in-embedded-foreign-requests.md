---
title: Traitement de variables dans des requêtes étrangères incorporées
description: Les références $var$ se trouvant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Traitement de variables dans des requêtes étrangères incorporées{#variable-processing-in-embedded-foreign-requests}

Toutes les références `$var$` qui se produisent n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes.

Permet de placer des requêtes étrangères incorporées dans un modèle dans un catalogue d’images.

Les valeurs de variable qui doivent être remplacées dans des requêtes étrangères doivent généralement être codées deux fois, car aucun réencodage n’est appliqué avant que le serveur ne tente de transmettre l’URL étrangère finale.
