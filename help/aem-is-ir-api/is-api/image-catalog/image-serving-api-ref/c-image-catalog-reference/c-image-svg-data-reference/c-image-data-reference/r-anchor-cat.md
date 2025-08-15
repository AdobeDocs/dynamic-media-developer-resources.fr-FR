---
description: Ancre d’image. Point d’origine lorsque cette image est utilisée comme calque dans un modèle ou une image composite.
solution: Experience Manager
title: Ancre
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---

# Ancre{#anchor}

Ancre d’image. Point d’origine lorsque cette image est utilisée comme calque dans un modèle ou une image composite.

Définit également le point central par défaut pour la rotation.

## Propriétés {#section-95740f14160744e7bc763094b8be40d8}

Deux nombres entiers, séparés par une virgule. Décalage des pixels par rapport au coin supérieur gauche de l’image pleine résolution.

Remplacé par `anchor=`(qui à son tour peut être remplacé par `origin=`).

## Par défaut {#section-ca3a4cc837d643519eff15951f2b47a1}

Le point central de l’image est utilisé si ce champ n’est pas présent ou s’il est vide, et s’il s’agit d’un enregistrement d’image valide (c’est-à-dire s’il `catalog::Path` est valide).

## Voir aussi {#section-f605d29c3f5d48ad8e2a374f11886f19}

[ancre=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origine=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
