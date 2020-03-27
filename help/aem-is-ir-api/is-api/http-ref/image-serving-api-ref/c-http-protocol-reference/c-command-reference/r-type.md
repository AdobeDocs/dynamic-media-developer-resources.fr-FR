---
description: Filtre de type de contenu statique. Spécifie une chaîne de filtre pour le contenu statique diffusé via /is/content.
seo-description: Filtre de type de contenu statique. Spécifie une chaîne de filtre pour le contenu statique diffusé via /is/content.
seo-title: type
solution: Experience Manager
title: type
topic: Scene7 Image Serving - Image Rendering API
uuid: 44906190-516c-481c-9714-bb19d77af33c
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# type{#type}

Filtre de type de contenu statique. Spécifie une chaîne de filtre pour le contenu statique diffusé via /is/content.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Entrez la chaîne de filtre. </p></td> 
 </tr> 
</table>

Le serveur compare la valeur de `catalog::Type` l’élément de contenu statique demandé. L’élément est renvoyé au client si les valeurs correspondent (sensible à la casse) ; dans le cas contraire, une erreur est renvoyée.

## Propriétés {#section-529b088434a44a9f86a64ef548d2925b}

Uniquement pris en charge pour les demandes de contenu statique (autres que les images) diffusées via. Ignoré si `catalog::Type` est vide ou non défini.

## Par défaut {#section-e9e8f51d0a01452183ccb510efd87d46}

Aucune correspondance de type n’est appliquée si `type=` l’élément n’est pas spécifié ou est vide.

## Voir aussi {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Diffusion du contenu](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da)statique (sans image), [catalogue:::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
