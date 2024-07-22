---
title: TrustedDomains
description: Domaines web d’application de Flash. Les applications de Flash Adobe peuvent nécessiter l’accès aux propriétés des images diffusées au format swf. Le swf doit accorder l’accès explicitement en enregistrant le nom des domaines d’application auxquels il fait confiance.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# TrustedDomains{#trusteddomains}

Domaines web d’application de Flash. Les applications de Flash Adobe peuvent nécessiter l’accès aux propriétés des images diffusées au format swf. Le swf doit accorder l’accès explicitement en enregistrant le nom des domaines d’application auxquels il fait confiance.

## Propriétés {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Chaîne contenant une liste de noms de domaine web séparés par des virgules. S’il est vide, les applications doivent être diffusées à partir du même domaine que le rendu d’image pour pouvoir accéder aux propriétés des images dans les réponses au format [!DNL swf].

## Par défaut {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Hérité de `default::TrustedDomains` si elle n’est pas présente.

## Voir aussi {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
