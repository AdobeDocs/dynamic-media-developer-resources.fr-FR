---
description: Domaines Web d’application de Flash. Les applications de Flash d’Adobe peuvent nécessiter l’accès aux propriétés des images fournies au format swf. Le fichier swf doit accorder l’accès explicitement en enregistrant le nom des domaines d’application auxquels il fait confiance.
seo-description: Domaines Web d’application de Flash. Les applications de Flash d’Adobe peuvent nécessiter l’accès aux propriétés des images fournies au format swf. Le fichier swf doit accorder l’accès explicitement en enregistrant le nom des domaines d’application auxquels il fait confiance.
seo-title: Domaines approuvés *
solution: Experience Manager
title: Domaines approuvés *
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c50180b1-9af7-45f1-878f-59f41f9958ae
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# Domaines approuvés *{#trusteddomains}

Domaines Web d’application de Flash. Les applications de Flash d’Adobe peuvent nécessiter l’accès aux propriétés des images fournies au format swf. Le fichier swf doit accorder l’accès explicitement en enregistrant le nom des domaines d’application auxquels il fait confiance.

## Propriétés {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Chaîne contenant une liste de noms de domaine Web séparés par des virgules. S’il est vide, les applications doivent être diffusées à partir du même domaine que le rendu des images pour pouvoir accéder aux propriétés des images dans des réponses [!DNL swf] au format PDF.

## Par défaut {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Hérité de `default::TrustedDomains` si elle n&#39;est pas présente.

## Voir aussi {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
