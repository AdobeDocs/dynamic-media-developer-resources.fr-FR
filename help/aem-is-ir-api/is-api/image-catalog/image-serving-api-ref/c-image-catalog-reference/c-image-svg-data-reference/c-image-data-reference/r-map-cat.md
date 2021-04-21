---
description: Données de zone cliquable. Aucun ou plusieurs éléments HTML <AREA> complets, triés recto verso.
solution: Experience Manager
title: Zone
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 5%

---


# Zone{#map}

Données de zone cliquable. Aucun ou plusieurs éléments HTML `<AREA>` complets, triés d’avant en arrière.

Le serveur interprète et peut modifier les attributs SHAPE et COORDS. (SHAPE=CIRCLE n’est pas pris en charge dans cette version.) Tous les autres attributs de `<AREA>` sont transmis sans modification. Les valeurs de coordonnées spécifiées avec l&#39;attribut COORDS doivent être des décalages de pixels à partir du coin supérieur gauche de l&#39;image source non modifiée. ( les coordonnées `%` ne sont pas prises en charge dans cette version et peuvent ne pas être traitées correctement.)

## Propriétés {#section-f52d89fd399b4356ac05277e6c12f956}

Valeur de chaîne de texte. S’il est spécifié, il doit s’agir d’un ou plusieurs éléments HTML `<AREA>` complets.

Ce champ participe à la localisation des chaînes de texte. Pour plus d&#39;informations, consultez la [Localisation de chaînes de texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) dans le *Guide de référence du protocole HTTP*.

## Par défaut {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Aucune

## Voir aussi {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ,  [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), Localisation de chaînes de  [texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
