---
title: imageSet
description: Visionneuse d’image. Spécifie une valeur de visionneuse d’images à utiliser lors de la génération de la réponse req=set.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 8%

---

# imageSet{#imageset}

Visionneuse d’image. Spécifie une valeur de visionneuse d’images à utiliser lors de la génération de la réponse req=set.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Chaîne de la visionneuse d’images. </p></td> 
 </tr> 
</table>

Pour échapper la valeur et garantir que les modificateurs inclus ne sont pas interprétés comme faisant partie de la chaîne de requête d’URL, la valeur entière doit être mise entre accolades. Si l’enregistrement de catalogue est spécifié dans le chemin d’accès net, cette valeur de modificateur remplace `catalog::ImageSet` de l’enregistrement principal. Pour une description de la syntaxe d’une visionneuse d’images valide, reportez-vous à la section `catalog::ImageSet` la documentation.

## Propriétés {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Attribut de requête. Facultatif. Remplacements `catalog::ImageSet` de l’enregistrement principal.

## Par défaut {#section-e8622ff40408450fb79d028f8d37fa6b}

Aucune

## Exemple {#section-68513d3c601f477399602a0741dab390}

Définition d’une visionneuse d’images à utiliser avec `req=set` request :

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## Voir aussi {#section-7e0320b2e09d475897082711a8f023a9}

[catalogue : ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) , [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Requêtes de visionneuse de médias](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
