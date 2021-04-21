---
description: Domaines Web d’application de Flash. Les applications de Flash d’Adobe peuvent nécessiter l’accès aux propriétés des images fournies avec fmt=swf ou fmt=swf3.
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 3%

---


# TrustedDomains{#trusteddomains}

Domaines Web d’application de Flash. Les applications de Flash d’Adobe peuvent nécessiter l’accès aux propriétés des images fournies avec fmt=swf ou fmt=swf3.

Le fichier swf doit accorder l’accès explicitement en enregistrant le nom des domaines d’application auxquels il fait confiance.

## Propriétés {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Chaîne contenant une liste de noms de domaine Web séparés par des virgules. S’ils sont vides, les applications doivent être diffusées à partir du même domaine que le rendu des images pour pouvoir accéder aux propriétés des images dans les réponses au format swf.

## Par défaut {#section-5c52ed3c7310488380f5a6f9540bf981}

Hérité de `default::TrustedDomains` si elle n&#39;est pas présente.

## Voir aussi {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
