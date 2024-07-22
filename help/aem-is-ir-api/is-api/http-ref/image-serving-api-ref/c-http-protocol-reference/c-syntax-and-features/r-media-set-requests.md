---
description: La diffusion d’images fournit un mécanisme permettant de récupérer une réponse de texte hiérarchique (xml ou json) qui représente toutes les ressources et métadonnées associées au catalogue ImageSet pour un enregistrement particulier.
solution: Experience Manager
title: Requêtes de visionneuse de médias
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# Requêtes de visionneuse de médias{#media-set-requests}

La diffusion d’images fournit un mécanisme permettant de récupérer une réponse de texte hiérarchique (xml ou json) qui représente toutes les ressources et métadonnées associées à catalog::ImageSet pour un enregistrement particulier.

Les visionneuses peuvent utiliser ce mécanisme pour générer des réponses afin d’informer la présentation d’images, de vidéos, de visionneuses de vidéos, d’échantillons, de visionneuses à 360°, de pages (catalogues électroniques) simples et de visionneuses de médias.

## Syntaxe de la requête {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

La réponse définie pour un `catalog::ImageSet` peut être récupérée à l’aide du modificateur `req=set` et en référençant l’ID d’enregistrement du catalogue dans le chemin d’accès net. Vous pouvez également spécifier la visionneuse d’images directement dans l’URL à l’aide du modificateur `imageset=`. Si le modificateur `imageset=` est utilisé pour spécifier la visionneuse d’images, l’ensemble de la valeur doit être entouré d’accolades afin d’échapper la valeur de la visionneuse d’images et de s’assurer que les modificateurs inclus ne sont pas interprétés comme faisant partie de la chaîne de requête d’URL.

## Types de réponses définies {#section-93eb0a1f70344da2a888e56372ad3896}

Le mécanisme d’ensemble prend en charge les types de réponses suivants :

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>images simples </p></td> 
  <td class="stentry"> <p>Un enregistrement d’image sans catalogue <span class="codeph"> ::ImageSet</span> défini. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>vidéos simples </p></td> 
  <td class="stentry"> <p>Enregistrement vidéo dans le catalogue de contenu statique. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ensembles d’échantillons </p></td> 
  <td class="stentry"> <p>Ensemble d’éléments constitué d’une référence à un enregistrement d’image et d’une référence séparée facultative à un enregistrement d’image utilisé comme échantillon. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>jeux d’échantillons hiérarchiques </p></td> 
  <td class="stentry"> <p>Ensemble d’éléments constitué d’un élément d’échantillon de base ou d’une référence à un enregistrement d’ensemble d’échantillons. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>visionneuses à 360° </p></td> 
  <td class="stentry"> <p>Un ensemble d’éléments constitué d’une liste simple d’identifiants d’image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>visionneuses à 360° bidimensionnelles </p></td> 
  <td class="stentry"> <p>Ensemble d’éléments constitué d’une image simple ou d’une référence à une visionneuse à 360° de base. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>jeux de pages </p></td> 
  <td class="stentry"> <p>Un ensemble d’éléments constitué d’une liste de trois images de page au maximum </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>visionneuses de médias </p></td> 
  <td class="stentry"> <p>Ensemble d’éléments constitué d’images simples, de visionneuses de vidéos, d’ensembles d’échantillons, d’ensembles d’échantillons hiérarchiques, de visionneuses à 360°, de visionneuses à 360° bidimensionnelles, de pages et de ressources vidéo. Chaque élément de visionneuse de médias peut également contenir un échantillon facultatif. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>visionneuses de vidéos </p></td> 
  <td class="stentry"> <p>Ensemble d’éléments consistant en une liste de vidéos simples. </p></td> 
 </tr> 
</table>

## Détection du type d&#39;ensemble extérieur {#section-3dd6e453528d46898e559d31458a59ba}

Lorsqu’une requête `req=set` est reçue, le type de réponse à générer est déterminé par la valeur de `catalog::AssetType`. Si `catalog::AssetType` n’est pas défini, le type de réponse est déterminé par les règles suivantes :

* Si l’enregistrement se trouve dans le catalogue d’images ET `catalog::ImageSet` est défini

   * Supposons qu’un jeu de catalogues électroniques soit défini si au moins une entrée dans le champ Visionneuse d’images d’enregistrement contient deux points
   * Supposons qu’un jeu de médias contienne au moins une entrée dans le champ Visionneuse d’images d’enregistrement contenant deux points-virgules.
   * Supposons que la visionneuse d’images contienne au moins une entrée dans le champ Visionneuse d’images d’enregistrement avec un point-virgule.
   * Supposons qu’une visionneuse à 360° ne contienne aucun signe deux-points ou point-virgule, mais qu’au moins une entrée contienne un jeu référencé ou un jeu en ligne (il s’agit d’une visionneuse à 360° en 2D).
   * Supposons qu’un ensemble soit inconnu si aucune entrée ne contient deux-points, un point-virgule, un ensemble référencé ou un ensemble en ligne (c’est-à-dire une liste d’images séparées par des virgules).

* Si l’enregistrement se trouve dans les catalogues d’image ET de contenu statique

   * Supposons que l’extension de fichier soit dans l’ensemble suivant : mp3, mp4, flv, f4v, swf, xml
   * Considérer autrement l’image

* Si l’enregistrement se trouve dans le catalogue de contenu statique mais PAS dans le catalogue d’images

   * Supposons que l’extension de fichier soit dans l’ensemble suivant : mp3, mp4, flv, f4v, swf, xml
   * Supposons qu’elles soient statiques dans d’autres cas

* Si l’enregistrement se trouve dans le catalogue d’images mais PAS dans le catalogue de contenu statique

   * Image d’hypothèse

* Si l’enregistrement est introuvable dans le catalogue d’images et INTROUVABLE dans le catalogue de contenu statique

   * Supposons que l’extension de fichier vidéo basée sur fichier soit dans l’ensemble suivant : mp3, mp4, flv, f4v, swf, xml
   * Exemple d’une image basée sur un fichier

Dans tous les cas, la réponse XML obtenue est conforme au document XML spécifié avec le noeud racine défini correspondant au type détecté.

## Détection du type d’ensemble interne {#section-8f46490e467247e69ce284704def06f3}

Lorsque l’ensemble externe est détecté en tant que type de visionneuse de médias, la réponse contient un ensemble d’éléments de visionneuse de médias correspondant à chaque entrée de visionneuse de médias dans `catalog::ImageSet`. Si le paramètre de type facultatif est spécifié pour une entrée de visionneuse de médias spécifique, il est mappé à un type de sortie selon le tableau suivant :

| Type d’entrée | Type de sortie |
|---|---|
| `img` | `img` |
| `basic` | `img` |
| `advanced_image` | `img` |
| `img_set` | `img_set` |
| `advanced_image_set` | `img_set` |
| `advanced_swatchset` | `img_set` |
| `spin` | `spin` |
| `video` | `video` |
| `video_set` | `video_set` |
| `static` | `static` |
| `ecat` | `ecat` |

Si le paramètre de type facultatif pour une entrée de visionneuse de médias spécifique n’est pas spécifié ou correspond à un type non pris en charge, le type d’élément de visionneuse de médias est automatiquement détecté à l’aide des mêmes règles que celles appliquées au niveau de l’ensemble externe.

## Spécification XML {#section-c1bd60948ef545759a16885bb6fcc607}

La réponse xml renvoyée est conforme à la spécification suivante :

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

Le modificateur `labelkey=` est utilisé avec le champ `catalog::UserData` pour générer des libellés pour les images et les échantillons. Le champ `catalog:UserData` est analysé sous la forme d’un ensemble de paires clé/valeur et les index de clé de libellé dans cet ensemble pour récupérer la valeur de la clé donnée. Cette valeur est ensuite renvoyée dans l’attribut *`l`* pour les *`s`* et *`i`*.

## Restrictions appliquées {#section-b9f042873bee45a5ae11b69fd42f2bca}

Pour limiter la taille de la réponse et empêcher les problèmes d’auto-référence, la profondeur d’imbrication maximale est contrôlée par la propriété de serveur `PS::fvctx.nestingLimit`. Si cette limite est dépassée, une erreur est renvoyée.

Afin de limiter la taille des réponses xml pour les jeux de catalogues électroniques volumineux, les métadonnées privées sont supprimées pour les éléments de jeu de brochures en fonction de la propriété de serveur `PS::fvctx.brochureLimit`. Toutes les métadonnées privées associées à la brochure sont exportées jusqu’à ce que la limite de la brochure soit atteinte. Une fois la limite dépassée, les mappages privés et les données utilisateur sont supprimés et un indicateur correspondant est défini pour indiquer le type de données supprimé.

Les visionneuses de médias imbriquées ne sont pas prises en charge. Une visionneuse de médias imbriquée est définie comme une visionneuse de médias qui contient un élément de visionneuse de médias de type visionneuse de médias. Si cette condition est détectée, une erreur est renvoyée.

## Exemples {#section-588c9d33aa05482c86cd2b1936887228}

Pour obtenir des exemples de réponses XML pour la requête `req=set`, consultez la page Propriétés sous l’en-tête Exemples d’HTML .

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Voir aussi {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [Référence du catalogue d’images](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
