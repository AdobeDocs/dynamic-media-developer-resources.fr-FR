---
description: Définissez la marge du média. Définit la marge du média définie dans le fichier PDF.
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
TQID: 'https://experienceleague.adobe.com/xbnVRTqP7h5vs3Cdlur8ge1nPz7rjGzpChCFDwue6U0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 57
ht-degree: 0%

---

# mediaMargin{#mediamargin}

Définissez la marge du média. Définit la marge du média définie dans le fichier PDF.

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` en points

Par défaut, la `mediaMargin` est définie sur la taille réelle du document définie par `viewWidth` et `viewHeight`. Les valeurs *[!DNL left]*, *[!DNL bottom]* et *[!DNL right]* sont définies par défaut sur la valeur *[!DNL top]* si elles ne sont pas spécifiées.
