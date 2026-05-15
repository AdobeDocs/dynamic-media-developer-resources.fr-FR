---
description: Les transformations sont appliquées aux calques d’images et de texte sources.
solution: Experience Manager
title: Transformations de calque
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
TQID: 'https://experienceleague.adobe.com/jChFcZzWWOlbicpu0WeRSJb608dGT9JmVSItV-uEjBY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 0%

---

# Transformations de calque{#layer-transforms}

Les transformations sont appliquées aux calques d’images et de texte sources.

Les opérations suivantes sont appliquées aux images sources, dans l&#39;ordre donné, pour obtenir la relation spatiale souhaitée avec la couche 0:

1. Appliquer le `crop=`, si spécifié.
1. Mise à l’échelle en fonction de `size=` ou, si `size=` n’est pas spécifié, en fonction de `scale=`, ou, si `scale=` n’est pas spécifié, en fonction de `res=`, ou, si `res=` n’est pas spécifié, utilisez l’image source en résolution complète.
1. Appliquer le `flip=`, si spécifié.
1. Appliquer le `rotate=`, si spécifié.
1. Appliquer le `extend=`, si spécifié.
1. Positionnez le calque dans la zone de travail en fonction des `origin=` et des `pos=` (voir ci-dessous).

Les transformations suivantes sont appliquées aux calques de texte :

1. La taille de la zone de texte est déterminée par `size=`, ou par la largeur et la hauteur du texte, si `size=` n’est que partiellement ou pas du tout fournie. Le texte est aligné dans la zone de texte à l’aide des attributs d’alignement de texte rtf. Le texte peut être recadré par la zone de texte.
1. Mettez à l’échelle le contenu texte en fonction de la résolution spécifiée avec `textAttr=`.
1. Appliquer le `rotate=`, si spécifié.
1. Appliquer le `extend=`, si spécifié.
1. Positionnez le calque dans la zone de travail en fonction des `origin=` et des `pos=` (voir ci-dessous).

Pour les calques d’image et de texte, la dernière étape de positionnement du calque dans la zone de travail ne s’applique pas au calque 0, puisque le calque 0 constitue effectivement la zone de travail.
