---
description: Outre le dimensionnement (size=) et le positionnement (pos=) des calques par rapport au calque 0 et la spécification de l’ordre de composition (l’ordre z) avec la commande layer=, les calques peuvent être pivotés (rotate=) et renversés (flip=).
seo-description: Outre le dimensionnement (size=) et le positionnement (pos=) des calques par rapport au calque 0 et la spécification de l’ordre de composition (l’ordre z) avec la commande layer=, les calques peuvent être pivotés (rotate=) et renversés (flip=).
seo-title: Opérations de couche
solution: Experience Manager
title: Opérations de couche
topic: Scene7 Image Serving - Image Rendering API
uuid: a9ef4199-cfa2-480e-a4de-8a0b9064a649
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Opérations de couche{#layer-operations}

Outre le dimensionnement (size=) et le positionnement (pos=) des calques par rapport au calque 0 et la spécification de l’ordre de composition (l’ordre z) avec la commande layer=, les calques peuvent être pivotés (rotate=) et renversés (flip=).

Les attributs `origin=` et `anchor=` peuvent être utilisés pour conserver l’alignement souhaité entre les calques lorsque les images ou le texte sont modifiés dynamiquement dans les modèles.

La commande `maskUse=` permet aux calques d’image d’accéder à la zone d’arrière-plan des images contenant des masques distincts.

`opac=` peut être utilisé pour varier l’opacité du calque et  `hide=` pour afficher ou masquer le calque.
