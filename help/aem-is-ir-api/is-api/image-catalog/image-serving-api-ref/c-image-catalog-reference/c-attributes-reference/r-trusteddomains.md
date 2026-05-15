---
description: Domaines web des applications Flash. Les applications Adobe Flash peuvent nécessiter l’accès aux propriétés des images diffusées avec fmt=swf ou fmt=swf3.
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
TQID: 'https://experienceleague.adobe.com/xGn-usdBOB3NjRaffq6w0SJDlDerpeQJHGhKej-L3Cw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 2%

---

# TrustedDomains{#trusteddomains}

Domaines web des applications Flash. Les applications Adobe Flash peuvent nécessiter l’accès aux propriétés des images diffusées avec fmt=swf ou fmt=swf3.

Le swf doit octroyer l&#39;accès de manière explicite en enregistrant le nom des domaines d&#39;application auxquels il fait confiance.

## Propriétés {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Chaîne contenant une liste de noms de domaines web séparés par des virgules. Si ce champ est vide, les applications doivent être diffusées à partir du même domaine que le rendu d’image pour pouvoir accéder aux propriétés des images dans les réponses au format SWF.

## Par défaut {#section-5c52ed3c7310488380f5a6f9540bf981}

Hérité de `default::TrustedDomains` s’il est absent.

## Voir aussi {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
