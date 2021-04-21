---
description: Dans la séquence de commandes de modificateur d’URL ou de catalogue, une séquence de définitions de calque se début avec la commande layer= et se termine par une autre commande layer=, une commande effect= ou la fin de l’URL.
solution: Experience Manager
title: Spécification de calques
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# Spécification des calques{#specifying-layers}

Dans la séquence de commandes URL ou catalog::Modificateur, une séquence de définitions de calque se début avec la commande layer= et se termine par une autre commande layer=, une commande effect= ou la fin de l’URL.

Toutes les commandes de la séquence de définition de calque sont associées au calque.

La commande `layer=` spécifie un numéro de calque, qui doit être un entier 0 ou plus. Toutes les commandes des séquences de définitions de calque portant le même numéro de calque sont appliquées au même calque. Si la même commande se produit plusieurs fois, la dernière instance prévaut.
