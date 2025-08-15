---
description: Masque d’image. Demande les données de masque (couche alpha).
solution: Experience Manager
title: masque
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# masque{#mask}

Masque d’image. Demande les données de masque (couche alpha).

`req=mask`

Prend en charge les mêmes commandes que `req=img`. Elles sont traitées de la même manière par le serveur, mais au lieu de renvoyer les données RVB ou RVBA, le serveur ignore les informations de couleur et renvoie uniquement les données de masque (couche alpha). Le format des données de réponse et le type MIME de réponse sont déterminés par `fmt=`.

La réponse HTTP peut être mise en cache avec la durée de vie basée sur la base de `catalog::Expiration`.
