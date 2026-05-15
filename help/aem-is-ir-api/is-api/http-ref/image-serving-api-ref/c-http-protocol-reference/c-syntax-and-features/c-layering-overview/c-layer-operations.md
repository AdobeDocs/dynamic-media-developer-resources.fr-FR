---
description: Outre le dimensionnement (size=) et le positionnement (pos=) des calques par rapport au calque 0 et la spécification de l’ordre de composition (ordre z) avec la commande layer=, les calques peuvent être pivotés (rotate=) et inversés (flip=).
solution: Experience Manager
title: Opérations de calque
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
TQID: 'https://experienceleague.adobe.com/uuGkOMzbkysv9BpR8zEK6dkuKgnseu3qwqLslA5W6zw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# Opérations de calque{#layer-operations}

Outre le dimensionnement (size=) et le positionnement (pos=) des calques par rapport au calque 0 et la spécification de l’ordre de composition (ordre z) avec la commande layer=, les calques peuvent être pivotés (rotate=) et inversés (flip=).

Les attributs `origin=` et `anchor=` peuvent être utilisés pour maintenir l’alignement souhaité entre les calques lorsque les images ou le texte sont modifiés dynamiquement dans les modèles.

La commande `maskUse=` permet aux calques d’image d’accéder à la zone d’arrière-plan des images qui comportent des masques distincts.

Vous pouvez utiliser `opac=` pour modifier l’opacité du calque et `hide=` afficher ou masquer le calque.
