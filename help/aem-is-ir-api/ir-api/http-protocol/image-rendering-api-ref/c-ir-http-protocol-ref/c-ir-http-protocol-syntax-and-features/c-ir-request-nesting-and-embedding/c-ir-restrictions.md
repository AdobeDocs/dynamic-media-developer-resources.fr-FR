---
title: Restrictions
description: Certaines restrictions s’appliquent pour l’imbrication et l’incorporation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# Restrictions{#restrictions}

Certaines restrictions s’appliquent pour l’imbrication et l’incorporation.

Pour de bonnes performances du serveur, la résolution des images renvoyées par les demandes imbriquées doit correspondre raisonnablement à la résolution de texture des objets auxquels le matériau est appliqué.

Les images étrangères sont mises en cache localement. Toute modification apportée à ces images n’est détectée que lorsque l’entrée du cache local devient obsolète (sur la base de l’en-tête HTTP expires).
