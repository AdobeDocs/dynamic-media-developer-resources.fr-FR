---
description: Visionneuse d’image. Spécifie une valeur de visionneuse d’images à utiliser lors de la génération de la réponse req=set.
seo-description: Visionneuse d’image. Spécifie une valeur de visionneuse d’images à utiliser lors de la génération de la réponse req=set.
seo-title: imageSet
solution: Experience Manager
title: imageSet
topic: Scene7 Image Serving - Image Rendering API
uuid: ecfb3905-e3ef-4ab8-a2c4-2c3f200e0f0f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# imageSet{#imageset}

Visionneuse d’image. Spécifie une valeur de visionneuse d’images à utiliser lors de la génération de la réponse req=set.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Chaîne de visionneuse d’images. </p></td> 
 </tr> 
</table>

Pour que la valeur soit ignorée et que les modificateurs inclus ne soient pas interprétés comme faisant partie de la chaîne de d’URL, la valeur entière doit être entourée d’accolades. Si l’enregistrement de catalogue est spécifié dans le chemin d’accès réseau, cette valeur de modificateur remplace `catalog::ImageSet` l’enregistrement principal. Pour obtenir une description de la syntaxe d’une visionneuse d’images valide, reportez-vous à la `catalog::ImageSet` documentation.

## Propriétés {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Attribut de requête. Facultatif. Remplace `catalog::ImageSet` l’enregistrement principal.

## Par défaut {#section-e8622ff40408450fb79d028f8d37fa6b}

Aucune

## Exemple {#section-68513d3c601f477399602a0741dab390}

Spécifiez la visionneuse d’images à utiliser avec `req=set` la requête :

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## Voir aussi {#section-7e0320b2e09d475897082711a8f023a9}

[catalogue ::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) , [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Demandes de visionneuse de [supports](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
