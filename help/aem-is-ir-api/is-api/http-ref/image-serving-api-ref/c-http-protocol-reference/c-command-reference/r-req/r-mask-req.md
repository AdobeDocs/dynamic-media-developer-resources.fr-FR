---
description: Masque d’image. Demande les données du masque (couche alpha).
solution: Experience Manager
title: masque
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
TQID: 'https://experienceleague.adobe.com/FMsQMZsc3N1ToEzXBE0vOzkezfemSzT6NaGJQ1gQqd8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# masque{#mask}

Masque d’image. Demande les données du masque (couche alpha).

`req=mask`

Prend en charge les mêmes commandes que `req=img`. Il est traité de la même manière par le serveur, mais au lieu de renvoyer les données RGB ou RGBA, le serveur ignore les informations de couleur et renvoie uniquement les données de masque (canal alpha). Le format des données de réponse et le type MIME de réponse sont déterminés par `fmt=`.

La réponse HTTP peut être mise en cache avec la TTL basée sur `catalog::Expiration`.
