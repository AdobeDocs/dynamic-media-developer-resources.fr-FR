---
description: Ancre d’image. Point d’Origine lorsque cette image est utilisée comme calque dans un modèle ou une image composite.
seo-description: Ancre d’image. Point d’Origine lorsque cette image est utilisée comme calque dans un modèle ou une image composite.
seo-title: Ancre
solution: Experience Manager
title: Ancre
uuid: 81069578-8470-4ec0-b755-47b0a8124024
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 5%

---


# Ancre{#anchor}

Ancre d’image. Point d’Origine lorsque cette image est utilisée comme calque dans un modèle ou une image composite.

Définit également le point central par défaut pour la rotation.

## Propriétés {#section-95740f14160744e7bc763094b8be40d8}

Deux nombres entiers, séparés par une virgule. Décalage des pixels par rapport au coin supérieur gauche de l’image à résolution totale.

Remplacé par `anchor=` (qui peut à son tour être remplacé par `origin=`).

## Par défaut {#section-ca3a4cc837d643519eff15951f2b47a1}

Le point central de l’image est utilisé si ce champ n’est pas présent ou s’il est vide et s’il s’agit d’un enregistrement d’image valide (c.-à-d. si `catalog::Path` est valide).

## Voir aussi {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ,  [origine=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
