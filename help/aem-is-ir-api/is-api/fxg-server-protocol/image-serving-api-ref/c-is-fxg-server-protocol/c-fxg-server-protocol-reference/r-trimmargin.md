---
description: Définissez la marge de rognage. Définit la marge de rognage définie dans le fichier PDF.
solution: Experience Manager
title: Marge de rognage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# Marge de rognage{#trimmargin}

Définissez la marge de rognage. Définit la marge de rognage définie dans le fichier PDF.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` en points

Par défaut, l’option `trimMargin` est définie sur la taille réelle du document définie par `viewWidth` et `viewHeight`. *[!DNL left]* *[!DNL bottom]* Si *[!DNL right]* elles ne sont pas spécifiées, les valeurs et sont définies par défaut sur la *[!DNL top]* valeur.
