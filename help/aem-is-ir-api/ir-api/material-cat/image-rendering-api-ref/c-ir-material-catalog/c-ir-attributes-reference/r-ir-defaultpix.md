---
title: DefaultPix
description: Taille par défaut de l’image de rendu. Le serveur oblige les images de réponse à ne pas dépasser ces valeurs de largeur et de hauteur, si la requête ne spécifie pas explicitement la taille d’affichage à l’aide des commandes wid= ou hei=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
TQID: 'https://experienceleague.adobe.com/n0m-j--YSFkdFmNOuJhRi3az-tARnc-N3sRmgkSJryE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 2%

---

# DefaultPix{#defaultpix}

Taille par défaut de l’image de rendu. Le serveur oblige les images de réponse à ne pas dépasser ces valeurs de largeur et de hauteur, si la requête ne spécifie pas explicitement la taille d’affichage à l’aide des commandes wid= ou hei=.

## Propriétés {#section-9dc5474fc75842308796ab6440b29611}

Deux nombres entiers, supérieurs ou égaux à zéro, séparés par une virgule. Largeur et hauteur en pixels. Vous pouvez définir les deux valeurs sur 0 pour qu’elles ne soient pas contraintes.

Non applicable aux requêtes imbriquées/incorporées.

## Par défaut {#section-1935781c561e4679aa87a5bcced8df90}

Hérité de `default::DefaultPix` si non défini ou si vide.

## Voir aussi {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)

