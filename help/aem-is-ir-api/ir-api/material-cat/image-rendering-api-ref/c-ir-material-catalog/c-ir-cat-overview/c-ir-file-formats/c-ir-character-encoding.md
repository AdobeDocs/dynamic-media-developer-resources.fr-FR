---
title: Encodage des caractères
description: Le rendu d’image prend en charge les catalogues de matériaux au codage ISO-8859-1 et UTF-8.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Encodage des caractères{#character-encoding}

Le rendu d’image prend en charge les catalogues de matériaux au codage ISO-8859-1 et UTF-8.

Une marque d&#39;ordre d&#39;octet (BOM) est utilisée pour spécifier le codage de chaque fichier. Pour UTF-8, la nomenclature est la séquence d&#39;octets `EF BB BF`. Le codage UTF-8 est supposé lorsque cette séquence de caractères est détectée au tout début de chaque fichier de catalogue de matières. Toute autre séquence d’octets entraîne l’interprétation du fichier comme étant codé selon la norme ISO-8859-1.

De nombreuses applications contemporaines, lorsqu&#39;elles sont configurées au format UTF-8, insèrent automatiquement la nomenclature.
