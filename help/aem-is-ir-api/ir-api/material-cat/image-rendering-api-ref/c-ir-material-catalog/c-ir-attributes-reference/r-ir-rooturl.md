---
title: RootUrl
description: URL racine pour les URL relatives d’images. Spécifie l’URL racine pour les URL relatives des images.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 3%

---

# RootUrl{#rooturl}

URL racine pour les URL relatives d’images. Spécifie l’URL racine pour les URL relatives des images. La propriété`attribute::RootUrl` est utilisée à la place de lorsqu’une `attribute::RootPath` `src=` valeur est entourée par {curly braces}.

## Propriétés {#section-69cd0f71ea614770a8778c745d23197a}

Valeur de chaîne de texte. Chemin d’accès racine d’URL absolu, y compris l’identifiant de protocole principal. Les protocoles suivants sont pris en charge : HTTP, HTTPS et FTP.

## Par défaut {#section-7a81569728474725a70f3a2cc4d48e85}

Hérité de `default::RootUrl` si non défini. Si elles sont définies mais vides, les URL relatives ne sont pas prises en charge par ce catalogue de matériaux.

## Voir aussi {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribut:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
