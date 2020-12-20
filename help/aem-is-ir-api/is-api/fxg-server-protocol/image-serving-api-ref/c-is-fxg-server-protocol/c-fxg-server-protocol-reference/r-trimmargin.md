---
description: Définissez la marge de rognage. Définit la marge de rognage définie dans le fichier PDF.
seo-description: Définissez la marge de rognage. Définit la marge de rognage définie dans le fichier PDF.
seo-title: trimMargin
solution: Experience Manager
title: trimMargin
topic: Scene7 Image Serving - Image Rendering API
uuid: af94f9e8-a32e-439a-817a-a40aa8dc7dd4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---


# trimMargin{#trimmargin}

Définissez la marge de rognage. Définit la marge de rognage définie dans le fichier PDF.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` points

Par défaut, `trimMargin` est défini sur la taille complète du document définie par `viewWidth` et `viewHeight`. Les valeurs *[!DNL left]*, *[!DNL bottom]* et *[!DNL right]* sont par défaut définies sur la valeur *[!DNL top]* si elles ne sont pas spécifiées.
