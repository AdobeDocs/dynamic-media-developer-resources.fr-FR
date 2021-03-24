---
description: Certaines restrictions s’appliquent à l’imbrication et à l’incorporation.
solution: Experience Manager
title: Restrictions
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# Restrictions{#restrictions}

Certaines restrictions s’appliquent à l’imbrication et à l’incorporation.

Pour de bonnes performances sur le serveur, la résolution des images renvoyées par les requêtes imbriquées doit raisonnablement correspondre à la résolution de texture des objets auxquels le matériau est appliqué.

Les images étrangères sont mises en cache localement. Les modifications apportées à ces images ne seront détectées qu’une fois que l’entrée de cache locale devient obsolète (en fonction de l’en-tête HTTP expires).
