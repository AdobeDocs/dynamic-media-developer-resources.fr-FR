---
description: Délai d’expiration par défaut du cache client. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue spécifique ne contient pas de valeur d’expiration de catalogue valide.
solution: Experience Manager
title: Expiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
TQID: 'https://experienceleague.adobe.com/NkQ-Bj-gHGksaD4Tmt7k8fYVEYfe67ACo4oWS25dKOE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 4%

---

# Expiration{#expiration}

Délai d’expiration par défaut du cache client. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue spécifique ne contiendrait aucune valeur catalog::Expiration valide.

## Propriétés {#section-063be3b2f13a48a3a5ab8080718e9812}

Nombre réel, supérieur ou égal à 0. Nombre d’heures avant expiration depuis la génération des données de réponse. Définissez la valeur sur 0 pour que l’image de réponse expire immédiatement, ce qui désactive efficacement la mise en cache du client. Définissez-le sur -1 pour marquer comme `never expire`.

## Par défaut {#section-f55308b195c04083996f6717c8537634}

Hérité de `default::Expiration` si non défini ou si vide.

La durée de vie (TTL) correspond à la durée avant l’expiration du cache. La durée de vie par défaut est de 10 heures.

## Voir aussi {#section-b2411d99ddb14115ad475d506efd8967}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
