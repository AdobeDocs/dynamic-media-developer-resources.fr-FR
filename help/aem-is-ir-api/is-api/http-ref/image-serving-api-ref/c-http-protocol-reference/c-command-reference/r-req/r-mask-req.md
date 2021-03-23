---
description: Masque d’image. Demande les données de masque (canal alpha).
seo-description: Masque d’image. Demande les données de masque (canal alpha).
seo-title: masque
solution: Experience Manager
title: masque
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 10%

---


# mask{#mask}

Masque d’image. Demande les données de masque (canal alpha).

`req=mask`

Prend en charge les mêmes commandes que `req=img` et est traité de la même manière par le serveur, mais au lieu de renvoyer les données RVB ou RVB, le serveur ignore les informations de couleur et renvoie uniquement les données de masque (canal alpha). Le format des données de réponse et le type MIME de réponse sont déterminés par `fmt=`.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.
