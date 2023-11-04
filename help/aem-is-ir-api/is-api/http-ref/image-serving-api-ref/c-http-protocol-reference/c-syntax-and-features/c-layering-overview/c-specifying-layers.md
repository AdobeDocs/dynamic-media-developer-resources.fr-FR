---
description: Dans la séquence de commande de modificateur d’URL ou de catalogue, une séquence de définition de calque commence par la commande layer= et se termine par une autre commande layer=, une commande d’effet= ou la fin de l’URL.
solution: Experience Manager
title: Spécification des calques
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# Spécification des calques{#specifying-layers}

Dans la séquence de commande URL ou catalogue ::Modifier , une séquence de définition de calque commence par la commande layer= et se termine par une autre commande layer=, une commande d’effet= ou la fin de l’URL.

Toutes les commandes de la séquence de définition de calque sont associées au calque.

La variable `layer=` spécifie un numéro de calque, qui doit être un nombre entier 0 ou supérieur. Toutes les commandes des séquences de définition de calque ayant le même numéro de calque sont appliquées au même calque. Si la même commande se produit plusieurs fois, la dernière instance l’emporte.
