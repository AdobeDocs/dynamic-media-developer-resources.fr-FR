---
description: Outre le dimensionnement (size=) et le positionnement (pos=) des calques par rapport au calque 0 et la spécification de l’ordre de composition (l’ordre z) avec la commande layer=, les calques peuvent être pivotés (rotate=) et renversés (flip=).
solution: Experience Manager
title: Opérations de couche
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# Opérations de couche{#layer-operations}

Outre le dimensionnement (size=) et le positionnement (pos=) des calques par rapport au calque 0 et la spécification de l’ordre de composition (l’ordre z) avec la commande layer=, les calques peuvent être pivotés (rotate=) et renversés (flip=).

Les attributs `origin=` et `anchor=` peuvent être utilisés pour conserver l’alignement souhaité entre les calques lorsque les images ou le texte sont modifiés dynamiquement dans les modèles.

La commande `maskUse=` permet aux calques d’image d’accéder à la zone d’arrière-plan des images contenant des masques distincts.

`opac=` peut être utilisé pour varier l’opacité du calque et  `hide=` pour afficher ou masquer le calque.
