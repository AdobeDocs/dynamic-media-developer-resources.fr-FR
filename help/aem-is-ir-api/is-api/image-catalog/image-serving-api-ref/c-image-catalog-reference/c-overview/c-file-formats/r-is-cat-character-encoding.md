---
description: Image Serving prend en charge les catalogues d’images avec codage ISO-8859-1 et UTF-8.
seo-description: Image Serving prend en charge les catalogues d’images avec codage ISO-8859-1 et UTF-8.
seo-title: Codage des caractères
solution: Experience Manager
title: Codage des caractères
topic: Scene7 Image Serving - Image Rendering API
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Character encoding{#character-encoding}

Image Serving prend en charge les catalogues d’images avec codage ISO-8859-1 et UTF-8.

Une marque d’ordre des octets (BOM) est utilisée pour spécifier le codage de chaque fichier. Pour UTF-8, la nomenclature est la séquence d’octets `EF BB BF`. Le codage UTF-8 est supposé lorsque cette séquence de caractères est détectée au tout début de chaque fichier de catalogue d’images. Toute autre séquence d’octets entraîne l’interprétation du fichier comme étant codé selon la norme ISO-8859-1.

De nombreuses applications contemporaines, lorsqu’elles sont configurées pour UTF-8, insèrent automatiquement la nomenclature.
