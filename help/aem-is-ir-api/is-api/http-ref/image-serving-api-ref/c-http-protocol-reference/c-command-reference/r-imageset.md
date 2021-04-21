---
description: Visionneuse d’image. Spécifie une valeur de visionneuse d’images à utiliser lors de la génération d’une réponse req=set.
solution: Experience Manager
title: imageSet
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 8%

---


# imageSet{#imageset}

Visionneuse d’image. Spécifie une valeur de visionneuse d’images à utiliser lors de la génération d’une réponse req=set.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Chaîne de visionneuse d’images. </p></td> 
 </tr> 
</table>

Pour que la valeur d’échappement soit définie et que les modificateurs inclus ne soient pas interprétés comme faisant partie de la chaîne de requête d’URL, la valeur entière doit être entourée d’accolades. Si l&#39;enregistrement catalogue est spécifié dans le chemin d&#39;accès réseau, cette valeur de modificateur remplace `catalog::ImageSet` par l&#39;enregistrement principal. Pour obtenir une description de la syntaxe d’une visionneuse d’images valide, consultez la documentation `catalog::ImageSet`.

## Propriétés {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Attribut de requête. Facultatif. Remplace `catalog::ImageSet` de l&#39;enregistrement principal.

## Par défaut {#section-e8622ff40408450fb79d028f8d37fa6b}

Aucune

## Exemple {#section-68513d3c601f477399602a0741dab390}

Spécifiez la visionneuse d’images à utiliser avec la demande `req=set` :

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## Voir aussi {#section-7e0320b2e09d475897082711a8f023a9}

[catalogue ::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) ,  [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Demandes  [de visionneuse de supports](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
