---
description: Définissez la marge de fond perdu. Définit la marge de fond perdu définie dans le fichier PDF.
solution: Experience Manager
title: Marge de fond perdu
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# Marge de fond perdu{#bleedmargin}

Définissez la marge de fond perdu. Définit la marge de fond perdu définie dans le fichier PDF.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` en points

Par défaut, l’option `bleedMargin` est définie sur la taille réelle du document définie par `viewWidth` et `viewHeight`. *[!DNL left]* *[!DNL bottom]* Si *[!DNL right]* elles ne sont pas spécifiées, les valeurs et sont définies par défaut sur la *[!DNL top]* valeur.
