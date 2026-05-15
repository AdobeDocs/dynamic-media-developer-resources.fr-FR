---
description: Si req = img, la taille de la toile de composition est entièrement déterminée par la taille de la couche 0.
solution: Experience Manager
title: Zone de travail de composition
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
TQID: 'https://experienceleague.adobe.com/62uvC05pApoYR5lY4A-KA5RHmW8Xz0r2-2yvOpdAkOo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 0%

---

# Zone de travail de composition{#the-compositing-canvas}

Si req = img, la taille de la toile de composition est entièrement déterminée par la taille de la couche 0.

Si la `size=` du calque 0 n’est pas spécifiée explicitement, les transformations de calque sont utilisées pour calculer la taille de la zone de travail de composition (voir ci-dessous).

Si `req=tmb`, la taille de la zone de travail de composition est déterminée par la `size=` spécifiée pour le calque 0 ou, si la taille n&#39;est pas spécifiée, la taille de la zone de travail de composition est définie sur la vue rect (voir ci-dessous).
