---
description: Données de zone cliquable. Aucun ou plusieurs éléments d’HTML complet <AREA>, triés recto verso.
solution: Experience Manager
title: Carte
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---

# Carte{#map}

Données de zone cliquable. Aucun ou plusieurs éléments d&#39;HTML `<AREA>` complets, triés de face en arrière.

Le serveur interprète et peut modifier les attributs SHAPE et COORDS (SHAPE=CIRCLE n’est pas pris en charge dans cette version). Tous les autres attributs de `<AREA>` sont transmis sans modification. Les valeurs de coordonnée spécifiées avec l’attribut COORDS doivent être des décalages de pixels à partir du coin supérieur gauche de l’image source non modifiée. (`%` les coordonnées ne sont pas prises en charge dans cette version et peuvent ne pas être traitées correctement.)

## Propriétés {#section-f52d89fd399b4356ac05277e6c12f956}

Valeur de chaîne de texte. S’il est spécifié, il doit s’agir d’un ou de plusieurs éléments d’HTML `<AREA>` complets.

Ce champ participe à la localisation de la chaîne de texte. Pour plus d’informations, reportez-vous à la section [Localisation de chaîne de texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) dans la *référence de protocole HTTP*.

## Par défaut {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Aucune

## Voir aussi {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Localisation de chaîne de texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
