---
description: Image Rendering prend en charge les catalogues de matériaux avec codage ISO-8859-1 et UTF-8.
seo-description: Image Rendering prend en charge les catalogues de matériaux avec codage ISO-8859-1 et UTF-8.
seo-title: Codage des caractères
solution: Experience Manager
title: Codage des caractères
uuid: efc3971b-dca1-4b47-a197-c10270ce17c9
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# Codage des caractères {#character-encoding}

Image Rendering prend en charge les catalogues de matériaux avec codage ISO-8859-1 et UTF-8.

Une marque d’ordre des octets (BOM) est utilisée pour spécifier le codage de chaque fichier. Pour UTF-8, la nomenclature est la séquence d’octets `EF BB BF`. Le codage UTF-8 est supposé lorsque cette séquence de caractères est détectée au tout début de chaque fichier catalogue de matières. Toute autre séquence d’octets entraîne l’interprétation du fichier comme étant codé selon la norme ISO-8859-1.

De nombreuses applications contemporaines, lorsqu&#39;elles sont configurées pour UTF-8, insèrent automatiquement la nomenclature.
