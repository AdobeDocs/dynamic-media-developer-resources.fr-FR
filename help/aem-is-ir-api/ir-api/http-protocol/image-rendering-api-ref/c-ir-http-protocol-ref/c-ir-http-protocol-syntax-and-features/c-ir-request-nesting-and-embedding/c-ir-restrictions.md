---
title: Restrictions
description: Certaines restrictions s’appliquent à l’imbrication et à l’incorporation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
TQID: 'https://experienceleague.adobe.com/rwy6ZnKA0pc-z-dqhsI0gD-FSqpqZr1bcIgJqtsjfIs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 0%

---

# Restrictions{#restrictions}

Certaines restrictions s’appliquent à l’imbrication et à l’incorporation.

Pour de bonnes performances du serveur, la résolution des images renvoyées par les requêtes imbriquées doit correspondre de manière raisonnable à la résolution de texture des objets auxquels la matière est appliquée.

Les images étrangères sont mises en cache localement. Les modifications apportées à ces images ne sont détectées qu’une fois que l’entrée du cache local devient obsolète (en fonction de l’en-tête HTTP expires).

