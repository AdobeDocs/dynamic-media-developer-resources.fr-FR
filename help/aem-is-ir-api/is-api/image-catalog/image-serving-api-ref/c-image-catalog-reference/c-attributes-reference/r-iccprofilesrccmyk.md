---
title: IccProfileSrcCmyk
description: Profil colorimétrique d’entrée CMJN par défaut. Indique le nom du profil colorimétrique ICC à utiliser pour les images sources CMJN qui n’incorporent pas de profil colorimétrique et pour certaines valeurs de couleur CMJN spécifiées avec différentes commandes de diffusion d’images, telles que color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
TQID: 'https://experienceleague.adobe.com/ZzJlJzNfiGnMaKHqMpoJmOiEobxRcHeNAw-B78S3o78'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 1%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

Profil colorimétrique d’entrée CMJN par défaut. Indique le nom du profil colorimétrique ICC à utiliser pour les images sources CMJN qui n’incorporent pas de profil colorimétrique et pour certaines valeurs de couleur CMJN spécifiées avec différentes commandes de diffusion d’images, telles que color=.

## Propriétés {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Chaîne de texte. Si spécifié, doit être une valeur de `icc::Name` valide de la carte de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou un chemin d’accès au fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil CMJN.

## Par défaut {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Hérité de `default::IccProfileSrcCmyk` si non défini ou si vide. Si `attribute::IccProfileSrcCmyk` ne correspond pas à un profil valide, `attribute::IccProfileCmyk` est utilisé à la place.

## Voir aussi {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
