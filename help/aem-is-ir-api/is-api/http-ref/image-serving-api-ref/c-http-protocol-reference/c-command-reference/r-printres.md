---
title: printRes
description: Résolution de l’impression. Il remplace la valeur de résolution d’impression incorporée dans l’image de réponse.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
TQID: 'https://experienceleague.adobe.com/QJMoF8XW-O1W-E12Cpix3uiwiqKOFo6A4bI6I0hv0II'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 2%

---

# printRes{#printres}

Résolution de l’impression. Il remplace la valeur de résolution d’impression incorporée dans l’image de réponse.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Résolution d’impression (dpi). </p></td> 
 </tr> 
</table>

La résolution d’impression est normalement définie par `catalog::PrintResolution` s’il s’agit d’une entrée de catalogue, sinon par la valeur de résolution d’impression incorporée dans l’image source. S’il existe un modèle ou une image composite superposée, la résolution d’impression par défaut incorporée dans le fichier de réponse est la résolution d’impression de l’image de calque avec le plus petit numéro de calque.

La définition de la résolution d’impression ne modifie pas la taille en pixels de l’image de réponse.

## Propriétés {#section-03c7910ebe234804a319e5d0d8ef3a74}

Attribut de requête. Il s’applique quel que soit le paramètre de calque actif.

## Par défaut {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution`
Ou la résolution d’impression incorporée dans l’image source.

## Voir aussi {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
