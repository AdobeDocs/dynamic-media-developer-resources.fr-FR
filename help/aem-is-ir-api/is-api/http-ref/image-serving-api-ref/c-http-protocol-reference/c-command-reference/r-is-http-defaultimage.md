---
description: Image de réponse par défaut. Indique l’image ou l’entrée de catalogue à utiliser lorsqu’une image est introuvable.
seo-description: Image de réponse par défaut. Indique l’image ou l’entrée de catalogue à utiliser lorsqu’une image est introuvable.
seo-title: defaultImage
solution: Experience Manager
title: defaultImage
topic: Scene7 Image Serving - Image Rendering API
uuid: 7478325c-9ac5-4b85-a4c5-5c495f924eb5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 2%

---


# defaultImage{#defaultimage}

Image de réponse par défaut. Indique l’image ou l’entrée de catalogue à utiliser lorsqu’une image est introuvable.

` defaultImage= *`objet`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objet  </span> </span> </p> </td> 
  <td class="stentry"> <p>Objet Image. </p> </td> 
 </tr> 
</table>

*`object`* peut être une entrée de catalogue (y compris un modèle) ou un simple chemin d’accès au fichier image. Utile pour remplacer les images manquantes par des images par défaut. Cette valeur remplace la valeur du catalogue correspondant `attribute::DefaultImage`. Une valeur vide ( `defaultImage=`) désactive la gestion des images par défaut.

>[!NOTE]
>
>Le mécanisme d’image par défaut ne s’applique pas aux objets SVG. Une erreur est renvoyée si l’objet SVG spécifié dans la requête est introuvable.

Si `attribute::DefaultImageMode=0`, *`object`* remplace l’intégralité de la requête d’origine, même si une seule image d’une composition à plusieurs images est manquante. Les seules commandes conservées à partir de la demande initiale sont les suivantes : `wid=`, `hei=`, `fmt=`, `qlt=`.

Si `attribute::DefaultImageMode=1`, l’objet remplace uniquement l’image de calque manquante ; les attributs de la couche manquante sont appliqués et le composite est traité et renvoyé comme d’habitude.

## Propriétés {#section-d30923d8dc4042eba10989212dd70887}

Attribut de requête. S’applique quel que soit le paramètre de calque actif. Ignoré si `req=` est différent de `img` ou `tmb`.

## Restrictions {#section-30df31bc8cac41cd917f1e45196779c2}

Les sources d’images étrangères ne sont pas couvertes par le mécanisme d’image par défaut ; une erreur est renvoyée si une source d’image étrangère n’est pas valide.

La diffusion d’images revient à `DefaultImageMode=0` en cas d’échec des demandes de rendu FXG ou de rendu Image Rendering imbriquées.

## Par défaut {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Voir aussi {#section-745392143c3747a2955e1ae561f58e5f}

[attribut::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [attribut: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
