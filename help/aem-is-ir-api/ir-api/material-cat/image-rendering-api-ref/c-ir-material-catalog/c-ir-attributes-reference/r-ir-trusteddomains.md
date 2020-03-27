---
description: Domaines Web d’application Flash. Les applications Adobe Flash peuvent nécessiter l’accès aux propriétés des images diffusées au format swf. Le fichier swf doit accorder l’accès explicitement en enregistrant le nom des domaines d’application auxquels il fait confiance.
seo-description: Domaines Web d’application Flash. Les applications Adobe Flash peuvent nécessiter l’accès aux propriétés des images diffusées au format swf. Le fichier swf doit accorder l’accès explicitement en enregistrant le nom des domaines d’application auxquels il fait confiance.
seo-title: Domaines approuvés *
solution: Experience Manager
title: Domaines approuvés *
topic: Scene7 Image Serving - Image Rendering API
uuid: c50180b1-9af7-45f1-878f-59f41f9958ae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Domaines approuvés *{#trusteddomains}

Domaines Web d’application Flash. Les applications Adobe Flash peuvent nécessiter l’accès aux propriétés des images diffusées au format swf. Le fichier swf doit accorder l’accès explicitement en enregistrant le nom des domaines d’application auxquels il fait confiance.

## Propriétés {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Chaîne contenant un de noms de domaine Web séparé par des virgules. S’il est vide, les applications doivent être diffusées à partir du même domaine que le rendu d’image pour pouvoir accéder aux propriétés des images dans les réponses [!DNL swf]formatées.

## Par défaut {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Hérité de `default::TrustedDomains` si non présent.

## Voir aussi {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
