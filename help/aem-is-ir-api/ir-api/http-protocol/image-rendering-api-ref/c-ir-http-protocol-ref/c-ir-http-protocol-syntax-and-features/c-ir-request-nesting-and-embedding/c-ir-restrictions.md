---
description: Certaines restrictions s’appliquent à l’imbrication et à l’incorporation.
seo-description: Certaines restrictions s’appliquent à l’imbrication et à l’incorporation.
seo-title: Restrictions
solution: Experience Manager
title: Restrictions
topic: Scene7 Image Serving - Image Rendering API
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Restrictions{#restrictions}

Certaines restrictions s’appliquent à l’imbrication et à l’incorporation.

Pour de bonnes performances sur le serveur, la résolution des images renvoyées par les requêtes imbriquées doit raisonnablement correspondre à la résolution de texture des objets auxquels le matériau est appliqué.

Les images étrangères sont mises en cache localement. Les modifications apportées à ces images ne seront détectées qu’une fois que l’entrée de cache locale devient obsolète (en fonction de l’en-tête HTTP d’expiration).
