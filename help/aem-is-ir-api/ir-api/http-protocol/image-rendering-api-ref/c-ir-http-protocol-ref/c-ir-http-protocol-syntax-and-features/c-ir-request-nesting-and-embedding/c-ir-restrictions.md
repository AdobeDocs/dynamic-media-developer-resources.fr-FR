---
description: Certaines restrictions s’appliquent à l’imbrication et à l’incorporation.
seo-description: Certaines restrictions s’appliquent à l’imbrication et à l’incorporation.
seo-title: Restrictions
solution: Experience Manager
title: Restrictions
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# Restrictions{#restrictions}

Certaines restrictions s’appliquent à l’imbrication et à l’incorporation.

Pour de bonnes performances sur le serveur, la résolution des images renvoyées par les requêtes imbriquées doit raisonnablement correspondre à la résolution de texture des objets auxquels le matériau est appliqué.

Les images étrangères sont mises en cache localement. Les modifications apportées à ces images ne seront détectées qu’une fois que l’entrée de cache locale devient obsolète (en fonction de l’en-tête HTTP expires).
