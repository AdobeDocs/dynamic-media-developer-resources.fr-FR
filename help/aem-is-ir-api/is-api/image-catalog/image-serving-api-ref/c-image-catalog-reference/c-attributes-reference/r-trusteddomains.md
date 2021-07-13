---
description: Domaines web d’application de Flash. Les applications de Flash Adobe peuvent nécessiter l’accès aux propriétés des images diffusées avec fmt=swf ou fmt=swf3.
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---

# TrustedDomains{#trusteddomains}

Domaines web d’application de Flash. Les applications de Flash Adobe peuvent nécessiter l’accès aux propriétés des images diffusées avec fmt=swf ou fmt=swf3.

Le swf doit accorder l’accès explicitement en enregistrant le nom des domaines d’application auxquels il fait confiance.

## Propriétés {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Chaîne contenant une liste de noms de domaine web séparés par des virgules. Si elles sont vides, les applications doivent être diffusées à partir du même domaine que le rendu d’image pour pouvoir accéder aux propriétés des images dans les réponses au format swf.

## Par défaut {#section-5c52ed3c7310488380f5a6f9540bf981}

Hérité de `default::TrustedDomains` si elle n’est pas présente.

## Voir aussi {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
