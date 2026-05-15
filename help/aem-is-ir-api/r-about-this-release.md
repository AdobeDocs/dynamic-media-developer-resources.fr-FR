---
description: Cette version (Image Serving 6.6.1 et Image Rendering 6.6.1) remplace Image Serving 6.5.3 et Image Rendering 6.5.3.
solution: Experience Manager
title: À propos de cette version
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
TQID: 'https://experienceleague.adobe.com/Mv84kHB7jsBYAvY1j--l8Ly5VZtKwFq-SsNdz2TIQOE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 1%

---

# À propos de cette version{#about-this-release}

Cette version (Image Serving 6.6.1 et Image Rendering 6.6.1) remplace Image Serving 6.5.3 et Image Rendering 6.5.3.

## Problèmes connus et changements de comportement {#section-9dbc05206187477f926a78e8108a34e1}

* L’utilisation du caractère de point d’interrogation dans les identifiants de ressources n’est plus prise en charge, même si le caractère est codé en URL.
* Les requêtes `/xfl/flash/` de bannières dynamiques ne sont plus prises en charge et renvoient désormais un code d’erreur HTTP 404.
* Les requêtes `/is/agm/` W2P ne sont plus prises en charge.
* Certains messages d’erreur ne s’affichent plus dans le navigateur. Par conséquent, vous devez consulter le journal de suivi pour le débogage.

## Nouvelles fonctionnalités {#section-b1386e36cb4544ebb79766a06b16842d}

* Échantillon intelligent
* Recadrage intelligent

## Correctif {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Correction d’un problème en raison duquel l’option `\qc` RTF suivie d’un espace empêchait le rendu d’une requête.
