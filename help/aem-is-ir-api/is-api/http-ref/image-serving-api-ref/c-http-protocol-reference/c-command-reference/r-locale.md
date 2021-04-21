---
description: ID de paramètre régional de traduction. Indique l’ID de paramètre régional de la requête.
solution: Experience Manager
title: local
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 4%

---


# locale{#locale}

ID de paramètre régional de traduction. Indique l’ID de paramètre régional de la requête.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>ID de paramètre régional (chaîne). </p></td> 
 </tr> 
</table>

A l’aide de cet identifiant et des règles spécifiées avec `attribute::LocaleMap` et `attribute::LocaleStrMap`, la diffusion d’images applique la traduction facultative de l’ID de catalogue et la localisation de chaînes.

## Propriétés {#section-1854a9902b884d9b8e8e713b6635723f}

Commande Request. S’applique à l’intégralité de la requête, y compris les requêtes imbriquées/incorporées, quel que soit l’endroit où elle est spécifiée. `locId` doit inclure uniquement des caractères ASCII imprimables. Ignoré si aucun mappage de localisation n’est défini dans le catalogue principal de cette requête. Une erreur est renvoyée si `locId` est vide ou non valide et qu&#39;aucune règle par défaut n&#39;est définie dans `attribute::DefaultLocale`.

## Par défaut {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` est utilisée lorsque locale= n’est pas spécifié.

## Voir aussi {#section-28a586d43ac4429d98e318a580c92af4}

[attribut::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) ,  [attribut::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318),  [attribut::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), prise en charge des Localisations
