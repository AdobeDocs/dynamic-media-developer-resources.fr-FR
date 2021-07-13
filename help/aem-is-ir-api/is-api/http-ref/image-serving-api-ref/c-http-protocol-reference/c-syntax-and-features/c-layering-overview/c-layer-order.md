---
description: Le numéro de calque détermine également l’ordre z.
solution: Experience Manager
title: Ordre de calque
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 3a8fdd55-6ac1-4bc9-935d-188ee60946d9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---

# Ordre de calque{#layer-order}

Le numéro de calque détermine également l’ordre z.

La couche 0 (couche d’arrière-plan) est requise ; les autres numéros de calque n’ont pas besoin d’être consécutifs. Ils seront tracés au-dessus du calque d’arrière-plan, dans l’ordre du numéro du calque ascendant. Le calque dont le numéro de calque est le plus élevé est rendu au-dessus et n’est jamais occulté par d’autres calques.
