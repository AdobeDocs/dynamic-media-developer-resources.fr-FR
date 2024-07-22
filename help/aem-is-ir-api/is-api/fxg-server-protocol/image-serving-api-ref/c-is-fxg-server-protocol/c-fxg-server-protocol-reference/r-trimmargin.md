---
description: Définissez la marge de rognage. Définit la marge de rognage définie dans le fichier du PDF.
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# trimMargin{#trimmargin}

Définissez la marge de rognage. Définit la marge de rognage définie dans le fichier du PDF.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` en points

Par défaut, `trimMargin` est défini sur la taille totale du document définie par `viewWidth` et `viewHeight`. Les valeurs *[!DNL left]*, *[!DNL bottom]* et *[!DNL right]* sont par défaut définies sur la valeur *[!DNL top]* si elles ne sont pas spécifiées.
