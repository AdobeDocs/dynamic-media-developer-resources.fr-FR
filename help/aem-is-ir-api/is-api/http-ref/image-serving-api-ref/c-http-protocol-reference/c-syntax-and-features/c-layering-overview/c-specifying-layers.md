---
description: Dans la séquence de commandes Modifier l’URL ou le catalogue, une séquence de définition de calque commence par la commande layer= et se termine par une autre commande layer=, une commande effect= ou la fin de l’URL.
solution: Experience Manager
title: Spécification des calques
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
TQID: 'https://experienceleague.adobe.com/jNFpOYrBFWWc53JvzwENSjpM-SkIpenxxWPUgGX-p0Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 0%

---

# Spécification des calques{#specifying-layers}

Dans la séquence de commandes URL ou catalog::Modifier, une séquence de définition de calque commence par la commande layer= et se termine par une autre commande layer=, une commande effect= ou la fin de l’URL.

Toutes les commandes de la séquence de définition de calque sont associées au calque.

La commande `layer=` spécifie un numéro de calque qui doit être un entier égal ou supérieur à 0. Toutes les commandes des séquences de définition de calque ayant le même numéro de calque sont appliquées au même calque. Si la même commande se produit plusieurs fois, la dernière instance prévaut.
