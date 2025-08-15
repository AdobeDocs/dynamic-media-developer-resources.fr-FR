---
description: Outre le dimensionnement (size=) et le positionnement (pos=) des calques par rapport au calque 0 et la spécification de l’ordre de composition (ordre z) avec la commande layer=, les calques peuvent être pivotés (rotate=) et inversés (flip=).
solution: Experience Manager
title: Opérations de calque
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Opérations de calque{#layer-operations}

Outre le dimensionnement (size=) et le positionnement (pos=) des calques par rapport au calque 0 et la spécification de l’ordre de composition (ordre z) avec la commande layer=, les calques peuvent être pivotés (rotate=) et inversés (flip=).

Les attributs `origin=` et `anchor=` peuvent être utilisés pour maintenir l’alignement souhaité entre les calques lorsque les images ou le texte sont modifiés dynamiquement dans les modèles.

La commande `maskUse=` permet aux calques d’image d’accéder à la zone d’arrière-plan des images qui comportent des masques distincts.

Vous pouvez utiliser `opac=` pour modifier l’opacité du calque et `hide=` afficher ou masquer le calque.
