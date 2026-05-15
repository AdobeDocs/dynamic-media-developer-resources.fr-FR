---
description: Précharger le cache du serveur. Exécute la requête comme req=img, mais au lieu de renvoyer l’image, le serveur renvoie la longueur de l’image de réponse (image.length), formatée en tant que données texte avec un type MIME text/plain.
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
TQID: 'https://experienceleague.adobe.com/Llp-0huLGkxBVxSgRngyAtNKqeHuZ02xJu71MM-Nqww'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# loadcache{#loadcache}

Précharger le cache du serveur. Exécute la requête comme req=img, mais au lieu de renvoyer l’image, le serveur renvoie la longueur de l’image de réponse (image.length), formatée en tant que données texte avec un type MIME text/plain.

`req=loadcache`

La réponse HTTP ne peut pas être mise en cache.

D’autres commandes de la requête s’appliquent comme indiqué.
