---
title: Traitement des variables dans des requêtes étrangères incorporées
description: Les références $var$ apparaissant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
TQID: 'https://experienceleague.adobe.com/-0KT9d6qz9-8d41vKNgbCYUKQQLBRaLE-0TFmyIvRCM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 0%

---

# Traitement des variables dans des requêtes étrangères incorporées{#variable-processing-in-embedded-foreign-requests}

Toutes les références `$var$` qui se produisent n&#39;importe où dans les accolades d&#39;une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes.

Permet de placer les requêtes étrangères incorporées dans un modèle de catalogue d’images.

Les valeurs de variable qui doivent être remplacées dans des requêtes étrangères doivent généralement être codées deux fois, car aucun recodage n’est appliqué avant que le serveur ne tente de transmettre l’url étrangère finale.

