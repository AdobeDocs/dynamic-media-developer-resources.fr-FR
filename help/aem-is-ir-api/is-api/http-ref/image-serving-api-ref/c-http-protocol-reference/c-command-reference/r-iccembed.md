---
title: iccEmbed
description: Incorporer le profil de couleurs. Indique si le profil colorimétrique ICC de travail ou le profil spécifié avec icc= doit être incorporé dans l’image de réponse.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc5637f6-5452-4bfb-bf30-def6f153f4ad
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# iccEmbed{#iccembed}

Incorporer le profil de couleurs. Indique si le profil colorimétrique ICC de travail ou le profil spécifié avec icc= doit être incorporé dans l’image de réponse.

`iccEmbed=0|1`

## Propriétés {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Attribut de requête. Ignoré si aucun profil n’est disponible pour l’incorporation.

## Par défaut {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`, sans incorporation de profils ICC dans les images de sortie. Ignoré si le format d’image de sortie ne prend pas en charge l’incorporation de profils ICC.

Voir [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) pour plus d’informations.

## Voir aussi {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) , [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
