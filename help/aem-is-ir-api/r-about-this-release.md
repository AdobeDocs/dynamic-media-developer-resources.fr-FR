---
description: Cette version (Image Serving 6.6.1 et Image Rendering 6.6.1) remplace Image Serving 6.5.3 et Image Rendering 6.5.3.
solution: Experience Manager
title: À propos de cette version
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---

# À propos de cette version{#about-this-release}

Cette version (Image Serving 6.6.1 et Image Rendering 6.6.1) remplace Image Serving 6.5.3 et Image Rendering 6.5.3.

## Problèmes connus et changements de comportement {#section-9dbc05206187477f926a78e8108a34e1}

* L’utilisation du caractère point d’interrogation dans les ID de ressources n’est plus prise en charge, même si le caractère est codé en URL.
* Les demandes de bannières `/xfl/flash/` dynamiques ne sont plus prises en charge et renvoient désormais un code d’erreur HTTP 404.
* Les requêtes W2P `/is/agm/` ne sont plus prises en charge.
* Certains messages d’erreur ne s’affichent plus dans le navigateur. En tant que tel, vous devez vérifier le journal de suivi à déboguer.

## Nouvelles fonctionnalités {#section-b1386e36cb4544ebb79766a06b16842d}

* Échantillon intelligent
* Recadrage intelligent

## Correction de bogue {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Correction d’un problème en raison duquel l’option RTF suivie d’un `\qc` espace empêchait le rendu d’une demande.
