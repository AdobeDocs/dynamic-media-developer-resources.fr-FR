---
description: Image Serving prend en charge les catalogues d’images avec codage ISO-8859-1 et UTF-8.
solution: Experience Manager
title: Codage des caractères
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Codage des caractères {#character-encoding}

Image Serving prend en charge les catalogues d’images avec codage ISO-8859-1 et UTF-8.

Une marque d’ordre des octets (BOM) est utilisée pour spécifier le codage de chaque fichier. Pour UTF-8, la nomenclature est la séquence d’octets `EF BB BF`. Le codage UTF-8 est supposé lorsque cette séquence de caractères est détectée au tout début de chaque fichier catalogue d’images. Toute autre séquence d’octets entraîne l’interprétation du fichier comme étant codé selon la norme ISO-8859-1.

De nombreuses applications contemporaines, lorsqu&#39;elles sont configurées pour UTF-8, insèrent automatiquement la nomenclature.
