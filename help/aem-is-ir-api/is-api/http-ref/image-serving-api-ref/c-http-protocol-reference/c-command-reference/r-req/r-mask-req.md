---
description: Masque d’image. Demande les données de masque (canal alpha).
solution: Experience Manager
title: masque
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 11%

---


# mask{#mask}

Masque d’image. Demande les données de masque (canal alpha).

`req=mask`

Prend en charge les mêmes commandes que `req=img`. Il est traité de la même manière par le serveur, mais au lieu de renvoyer les données RVB ou RVB, le serveur ignore les informations de couleur et renvoie uniquement les données de masque (canal alpha). Le format des données de réponse et le type MIME de réponse sont déterminés par `fmt=`.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.
