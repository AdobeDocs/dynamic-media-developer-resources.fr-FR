---
description: La diffusion d’images prend en charge les catalogues d’images avec codage ISO-8859-1 et UTF-8.
solution: Experience Manager
title: Encodage des caractères
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Encodage des caractères{#character-encoding}

La diffusion d’images prend en charge les catalogues d’images avec codage ISO-8859-1 et UTF-8.

Une marque d’ordre des octets (BOM) est utilisée pour spécifier le codage de chaque fichier. Pour UTF-8, la nomenclature est la séquence d’octets `EF BB BF`. Le codage UTF-8 est supposé lorsque cette séquence de caractères est détectée au tout début de chaque fichier de catalogue d’images. Pour toute autre séquence d’octets, le fichier est interprété comme étant codé selon la norme ISO-8859-1.

De nombreuses applications contemporaines, lorsqu’elles sont configurées pour UTF-8, insèrent automatiquement la nomenclature.
