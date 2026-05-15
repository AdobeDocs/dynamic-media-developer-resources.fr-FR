---
title: xmpEmbed
description: Incorporez des métadonnées XMP. Indique si les métadonnées XMP doivent être incluses dans l’image de réponse.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
TQID: 'https://experienceleague.adobe.com/2pISbWU-Y-4szY0jmZswDIxvBrPlJ1yZmQby0sZ1v-o'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 2%

---

# xmpEmbed{#xmpembed}

Incorporez des métadonnées XMP. Indique si les métadonnées XMP doivent être incluses dans l’image de réponse.

`xmpEmbed=0|1`

>[!NOTE]
>
>Les données XMP sont transmises de l’image source à l’image de réponse sans modification. Cela peut entraîner l’incorporation de données incorrectes dans l’image de réponse.

## Propriétés {#section-27024c4272f44d9a8c264a0629193af2}

Attribut de requête. Ignoré si l’image source ne contient pas de données XMP. Seules les données XMP provenant de l’image source de `layer=0` sont traitées. Les données XMP des autres images de calque sont ignorées.

Ignoré si le format de l’image de sortie ne prend pas en charge l’incorporation XMP. Reportez-vous à la description de `fmt=` pour obtenir une liste des formats d’image de sortie qui prennent en charge l’incorporation de XMP.

## Par défaut {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, pour l’absence d’incorporation de chemins dans les images de sortie.

## Voir aussi {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
