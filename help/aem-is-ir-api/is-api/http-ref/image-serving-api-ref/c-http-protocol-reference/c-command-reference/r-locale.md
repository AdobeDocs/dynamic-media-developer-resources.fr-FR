---
title: local
description: ID Des Paramètres Régionaux De Traduction. Indique l’ID de paramètre régional de la requête.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# local{#locale}

ID Des Paramètres Régionaux De Traduction. Indique l’ID de paramètre régional de la requête.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>ID de paramètre régional (chaîne). </p></td> 
 </tr> 
</table>

En utilisant cet identifiant et les règles spécifiées avec `attribute::LocaleMap` et `attribute::LocaleStrMap`, le serveur d’images applique la traduction facultative de l’identifiant de catalogue et la localisation de chaîne.

## Propriétés {#section-1854a9902b884d9b8e8e713b6635723f}

Request, commande S’applique à l’ensemble de la requête, y compris les requêtes imbriquées/incorporées, quel que soit l’endroit où elle est spécifiée. `locId` ne doit inclure que des caractères ASCII imprimables. Ignoré si aucune map de localisation n’est définie dans le catalogue principal de cette requête. Une erreur est renvoyée si vide ou non valide `locId` est spécifié et qu&#39;aucune règle par défaut n&#39;est définie dans `attribute::DefaultLocale`.

## Par défaut {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` est utilisé lorsque locale= n’est pas spécifié.

## Voir aussi {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), Prise en charge de la localisation
