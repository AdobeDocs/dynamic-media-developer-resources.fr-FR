---
description: Dans la séquence de commande de modificateur d’URL ou de catalogue, une séquence de définition de calque commence par la commande layer= et se termine par une autre commande layer=, une commande d’effet= ou la fin de l’URL.
solution: Experience Manager
title: Spécification des calques
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Spécification des calques{#specifying-layers}

Dans la séquence de commande URL ou catalogue ::Modifier , une séquence de définition de calque commence par la commande layer= et se termine par une autre commande layer=, une commande d’effet= ou la fin de l’URL.

Toutes les commandes de la séquence de définition de calque sont associées au calque.

La commande `layer=` spécifie un numéro de calque, qui doit être un entier 0 ou supérieur. Toutes les commandes des séquences de définition de calque ayant le même numéro de calque sont appliquées au même calque. Si la même commande se produit plusieurs fois, la dernière instance prévaut.
