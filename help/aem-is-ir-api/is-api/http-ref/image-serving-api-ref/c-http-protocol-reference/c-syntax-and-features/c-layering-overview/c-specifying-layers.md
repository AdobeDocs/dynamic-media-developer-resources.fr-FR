---
description: Dans la séquence de commandes de modificateur d’URL ou de catalogue, une séquence de définitions de calque se début avec la commande layer= et se termine par une autre commande layer=, une commande effect= ou la fin de l’URL.
seo-description: Dans la séquence de commandes de modificateur d’URL ou de catalogue, une séquence de définitions de calque se début avec la commande layer= et se termine par une autre commande layer=, une commande effect= ou la fin de l’URL.
seo-title: Spécification de calques
solution: Experience Manager
title: Spécification de calques
topic: Scene7 Image Serving - Image Rendering API
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# Spécification des calques{#specifying-layers}

Dans la séquence de commandes URL ou catalog::Modificateur, une séquence de définitions de calque se début avec la commande layer= et se termine par une autre commande layer=, une commande effect= ou la fin de l’URL.

Toutes les commandes de la séquence de définition de calque sont associées au calque.

La commande `layer=` spécifie un numéro de calque, qui doit être un entier 0 ou plus. Toutes les commandes des séquences de définitions de calque portant le même numéro de calque sont appliquées au même calque. Si la même commande se produit plusieurs fois, la dernière instance prévaut.
