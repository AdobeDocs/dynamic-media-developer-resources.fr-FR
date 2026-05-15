---
description: TTL de cache client pour les réponses d’image par défaut. Fournit l’intervalle d’expiration pour les réponses d’image par défaut (réponses qui renvoient une image par défaut spécifiée avec defaultImage= ou l’attribut DefaultImage).
solution: Experience Manager
title: Expiration par défaut
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
TQID: 'https://experienceleague.adobe.com/v-wtXCBtpHpf9mTjoQ58GZ9eXq-yR2tpGT0Kd-DTyNI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 1%

---

# Expiration par défaut{#defaultexpiration}

TTL de cache client pour les réponses d’image par défaut. Fournit l’intervalle d’expiration pour les réponses d’image par défaut (réponses qui renvoient une image par défaut spécifiée avec defaultImage= ou attribute::DefaultImage).

Appliqué uniquement lorsque l’image par défaut n’est pas associée à un enregistrement de catalogue ou lorsque l’enregistrement de catalogue d’images par défaut ne fournit pas de valeur de `catalog::Expiration` spécifique.

## Propriétés {#section-e564512476604fd7b964f9f2903d6d33}

Nombre réel, supérieur ou égal à 0. Nombre d’heures avant expiration depuis la génération des données de réponse. Définissez la valeur sur 0 pour que l’image de réponse expire immédiatement, ce qui désactive la mise en cache du client pour les réponses d’image par défaut. Définissez sur `-1` pour marquer comme `never expire`.

## Par défaut {#section-131cd32c2e214391857dba5af321f8cd}

Hérité de `default::DefaultExpiration` si non défini ou si vide.

La durée de vie (TTL) correspond à la durée avant l’expiration du cache. La durée de vie par défaut est de 1 heure.

## Voir aussi {#section-d8642c22e3d947129367dd76366963d6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
