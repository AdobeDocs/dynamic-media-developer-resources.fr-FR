---
description: Cette version (Image Serving 6.6.1 et Image Rendering 6.6.1) remplace Image Serving 6.5.3 et Image Rendering 6.5.3.
seo-description: Cette version (Image Serving 6.6.1 et Image Rendering 6.6.1) remplace Image Serving 6.5.3 et Image Rendering 6.5.3.
seo-title: A propos de cette version
solution: Experience Manager
title: A propos de cette version
topic: Scene7 Image Serving - Image Rendering API
uuid: 2fdd8920-433b-405e-bf93-dbef5735be3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
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

