---
title: printRes
description: Résolution d’impression. Permet de remplacer la valeur de résolution d’impression incorporée dans l’image de réponse.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# printRes{#printres}

Résolution d’impression. Permet de remplacer la valeur de résolution d’impression incorporée dans l’image de réponse.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Résolution d’impression (ppp). </p></td> 
 </tr> 
</table>

La résolution d’impression est normalement définie par `catalog::PrintResolution` dans le cas d’une entrée de catalogue, sinon par la valeur de résolution d’impression incorporée dans l’image source. Dans le cas d’un modèle ou d’une image composite superposée, la résolution d’impression par défaut incorporée dans le fichier de réponse est la résolution d’impression de l’image de calque dont le numéro de couche est le plus petit.

La définition de la résolution d’impression ne modifie pas la taille en pixels de l’image de réponse.

## Propriétés {#section-03c7910ebe234804a319e5d0d8ef3a74}

Attribut de requête. S’applique quel que soit le paramètre de calque actif.

## Par défaut {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` ou la résolution d’impression incorporée dans l’image source.

## Voir aussi {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalogue ::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
