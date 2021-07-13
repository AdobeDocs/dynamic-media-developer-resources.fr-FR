---
description: Certaines restrictions s’appliquent à l’imbrication et à l’incorporation.
solution: Experience Manager
title: Restrictions
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# Restrictions{#restrictions}

Certaines restrictions s’appliquent à l’imbrication et à l’incorporation.

Pour de bonnes performances du serveur, la résolution des images renvoyées par les demandes imbriquées doit raisonnablement correspondre à la résolution de texture du ou des objets auxquels la matière est appliquée.

Les images étrangères sont mises en cache localement. Toutes les modifications apportées à ces images seront détectées uniquement une fois que l’entrée de cache locale deviendra obsolète (en fonction de l’en-tête HTTP expires).
