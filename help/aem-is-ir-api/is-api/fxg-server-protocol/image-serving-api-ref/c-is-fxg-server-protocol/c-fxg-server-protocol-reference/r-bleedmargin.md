---
description: Définissez la marge de fond perdu. Définit la marge de fond perdu définie dans le fichier du PDF.
solution: Experience Manager
title: bleedmargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# bleedmargin{#bleedmargin}

Définissez la marge de fond perdu. Définit la marge de fond perdu définie dans le fichier du PDF.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` en points

Par défaut, `bleedMargin` est défini sur la taille totale du document définie par `viewWidth` et `viewHeight`. Les valeurs *[!DNL left]*, *[!DNL bottom]* et *[!DNL right]* sont par défaut définies sur la valeur *[!DNL top]* si elles ne sont pas spécifiées.
