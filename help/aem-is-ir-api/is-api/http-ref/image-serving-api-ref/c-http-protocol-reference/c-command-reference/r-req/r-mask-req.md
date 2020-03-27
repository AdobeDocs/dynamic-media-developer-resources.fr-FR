---
description: Masque d’image. Demande les données de masque (alpha).
seo-description: Masque d’image. Demande les données de masque (alpha).
seo-title: masquer
solution: Experience Manager
title: masquer
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mask{#mask}

Masque d’image. Demande les données de masque (alpha).

`req=mask`

Prend en charge les mêmes commandes que `req=img`et est traité de la même manière par le serveur, mais au lieu de renvoyer les données RVB ou RVB, le serveur ignore les informations de couleur et renvoie uniquement les données de masque (alpha). Le format des données de réponse et le type MIME de réponse sont déterminés par `fmt=`.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.
