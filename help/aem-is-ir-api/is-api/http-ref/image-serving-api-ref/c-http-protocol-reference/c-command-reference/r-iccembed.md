---
description: Incorporer le Profil de couleurs. Indique si le profil de couleurs ICC actif ou le profil spécifié avec icc= doit être incorporé dans l’image de réponse.
solution: Experience Manager
title: iccEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---


# iccEmbed{#iccembed}

Incorporer le Profil de couleurs. Indique si le profil de couleurs ICC actif ou le profil spécifié avec icc= doit être incorporé dans l’image de réponse.

`iccEmbed=0|1`

## Propriétés {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Attribut de requête. Ignoré si aucun profil n’est disponible pour l’incorporation.

## Par défaut {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`, pour ne pas incorporer de profils ICC dans les images de sortie. Ignoré si le format d’image de sortie ne prend pas en charge l’incorporation de profils ICC.

Voir [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) pour plus de détails.

## Voir aussi {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attribut ::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) ,  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
