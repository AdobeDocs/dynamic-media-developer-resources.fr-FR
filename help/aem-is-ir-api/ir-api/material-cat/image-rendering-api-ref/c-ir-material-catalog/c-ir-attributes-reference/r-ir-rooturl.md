---
title: RootURL
description: URL racine pour les URL d’image relatives. Spécifie l’URL racine pour les URL d’image relatives.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# RootURL{#rooturl}

URL racine pour les URL d’image relatives. Spécifie l’URL racine pour les URL d’image relatives. `attribute::RootUrl` est utilisé à la place de `attribute::RootPath` lorsqu’une valeur `src=` est entourée de { accolades }.

## Propriétés {#section-69cd0f71ea614770a8778c745d23197a}

Valeur de chaîne de texte. Chemin d’accès racine URL absolu, y compris l’identifiant de protocole de début. Les protocoles suivants sont pris en charge : HTTP, HTTPS et FTP.

## Par défaut {#section-7a81569728474725a70f3a2cc4d48e85}

Hérité de `default::RootUrl` si elle n’est pas définie. Si elles sont définies mais vides, les URL relatives ne sont pas prises en charge par ce catalogue matériel.

## Voir aussi {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
