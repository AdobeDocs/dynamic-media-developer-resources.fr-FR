---
description: Données de la zone cliquable. Aucun ou plusieurs éléments HTML <AREA> complets, triés de l’avant vers l’arrière.
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

Données de la zone cliquable. Aucun ou plusieurs éléments HTML `<AREA>` complets, triés de face à face.

Le serveur interprète et peut modifier les attributs SHAPE et CORDS (SHAPE=CIRCLE n&#39;est pas pris en charge dans cette version). Tous les autres attributs de `<AREA>` sont transmis sans modification. Les valeurs de coordonnées spécifiées avec l’attribut CORDS doivent être des décalages en pixels du coin supérieur gauche de l’image source non modifiée. (les coordonnées `%` ne sont pas prises en charge dans cette version et peuvent ne pas être traitées correctement.)

## Propriétés {#section-f52d89fd399b4356ac05277e6c12f956}

Valeur de chaîne de texte. S’il est spécifié, il doit s’agir d’un ou de plusieurs éléments HTML `<AREA>` complets.

Ce champ participe à la localisation de la chaîne de texte. Pour plus d’informations[&#x200B; consultez la section &#x200B;](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)Localisation de chaîne de texte dans la section *Référence du protocole HTTP*.

## Par défaut {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Aucune

## Voir aussi {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
