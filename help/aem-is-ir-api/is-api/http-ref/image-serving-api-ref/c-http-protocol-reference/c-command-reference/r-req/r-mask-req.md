---
description: Masque de l'image. Demande les données du masque (canal alpha).
solution: Experience Manager
title: mask
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 12%

---

# mask{#mask}

Masque de l&#39;image. Demande les données du masque (canal alpha).

`req=mask`

Prend en charge les mêmes commandes que `req=img`. Il est traité de la même manière par le serveur, mais au lieu de renvoyer les données RVB ou RVB, le serveur ignore les informations de couleur et renvoie uniquement les données de masque (couche alpha). Le format des données de réponse et le type MIME de réponse sont déterminés par `fmt=`.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.
