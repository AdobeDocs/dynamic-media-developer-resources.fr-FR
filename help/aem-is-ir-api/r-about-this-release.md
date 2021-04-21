---
description: Cette version (Image Serving 6.6.1 et Image Rendering 6.6.1) remplace Image Serving 6.5.3 et Image Rendering 6.5.3.
solution: Experience Manager
title: A propos de cette version
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# A propos de cette version{#about-this-release}

Cette version (Image Serving 6.6.1 et Image Rendering 6.6.1) remplace Image Serving 6.5.3 et Image Rendering 6.5.3.

## Problèmes connus et changements de comportement {#section-9dbc05206187477f926a78e8108a34e1}

* L’utilisation du caractère de point d’interrogation dans les ID de fichier n’est plus prise en charge, même si le caractère est codé en URL.
* Les requêtes de bannière dynamique `/xfl/flash/` ne sont plus prises en charge et renvoient désormais un code d’erreur http 404.
* Les requêtes W2P `/is/agm/` ne sont plus prises en charge.
* Certains messages d’erreur ne s’affichent plus dans le navigateur. Vous devez donc consulter le journal de suivi à déboguer.

## Nouvelles fonctionnalités {#section-b1386e36cb4544ebb79766a06b16842d}

* Nuance intelligente
* Recadrage intelligent

## Correctif {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Correction d’un problème en raison duquel l’option RTF `\qc` suivie d’un espace empêchait le rendu d’une requête.

