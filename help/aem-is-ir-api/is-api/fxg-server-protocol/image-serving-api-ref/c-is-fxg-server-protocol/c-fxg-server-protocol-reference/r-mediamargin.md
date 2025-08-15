---
description: Définissez la marge du média. Définit la marge du média définie dans le fichier PDF.
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# mediaMargin{#mediamargin}

Définissez la marge du média. Définit la marge du média définie dans le fichier PDF.

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` en points

Par défaut, la `mediaMargin` est définie sur la taille réelle du document définie par `viewWidth` et `viewHeight`. Les valeurs *[!DNL left]*, *[!DNL bottom]* et *[!DNL right]* sont définies par défaut sur la valeur *[!DNL top]* si elles ne sont pas spécifiées.
