---
description: La diffusion d’images fournit un mécanisme permettant de récupérer une réponse de texte hiérarchique (xml ou json) qui représente toutes les ressources et métadonnées associées au catalogue ImageSet pour un enregistrement particulier.
seo-description: La diffusion d’images fournit un mécanisme permettant de récupérer une réponse de texte hiérarchique (xml ou json) qui représente toutes les ressources et métadonnées associées au catalogue ImageSet pour un enregistrement particulier.
seo-title: Requêtes de visionneuse de supports
solution: Experience Manager
title: Requêtes de visionneuse de supports
topic: Scene7 Image Serving - Image Rendering API
uuid: af9fabcd-531d-43fb-bd97-269923bea5e8
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# Requêtes de visionneuse de supports{#media-set-requests}

La diffusion d’images fournit un mécanisme permettant de récupérer une réponse de texte hiérarchique (xml ou json) qui représente toutes les ressources et métadonnées associées à catalog::ImageSet pour un enregistrement particulier.

Les utilisateurs peuvent utiliser ce mécanisme pour générer des réponses afin d’informer la présentation de simples images, vidéos, visionneuses de vidéos, visionneuses d’échantillons, visionneuses à 360°, visionneuses de pages (catalogues électroniques) et visionneuses de supports.

## Syntaxe de requête {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

La réponse définie pour un `catalog::ImageSet` peut être récupérée à l’aide du `req=set` modificateur et en référençant l’ID d’enregistrement du catalogue dans le chemin d’accès réseau. Vous pouvez également spécifier la visionneuse d’images directement dans l’URL à l’aide du `imageset=` modificateur. Si le `imageset=` modificateur est utilisé pour spécifier la visionneuse d’images, la valeur entière doit être entourée d’accolades afin d’échapper à la valeur de la visionneuse d’images et de s’assurer que les modificateurs inclus ne sont pas interprétés comme faisant partie de la chaîne de d’URL.

## Types de réponses définies {#section-93eb0a1f70344da2a888e56372ad3896}

Le mécanisme d’ensemble prend en charge les types de réponses suivants :

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>images simples </p></td> 
  <td class="stentry"> <p>Un enregistrement d’image sans <span class="codeph"> catalogue::ImageSet</span> défini. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>vidéos simples </p></td> 
  <td class="stentry"> <p>Enregistrement vidéo dans le catalogue de contenu statique. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>jeux d’échantillons </p></td> 
  <td class="stentry"> <p>Ensemble d’éléments constitué d’une référence à un enregistrement d’image et d’une référence distincte facultative à un enregistrement d’image utilisé comme échantillon. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>jeux d’échantillons hiérarchiques </p></td> 
  <td class="stentry"> <p>Ensemble d’éléments constitué d’un élément d’échantillon de base ou d’une référence à un enregistrement d’ensemble d’échantillons. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>visionneuse à 360° </p></td> 
  <td class="stentry"> <p>Ensemble d’éléments constitué d’un simple d’ID d’image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>visionneuse à 360° bidimensionnelle </p></td> 
  <td class="stentry"> <p>Ensemble d’éléments constitué d’une image simple ou d’une référence à une visionneuse à 360° de base. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>jeux de pages </p></td> 
  <td class="stentry"> <p>Ensemble d’éléments constitué d’un  de trois images de page au maximum </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>visionneuse de supports </p></td> 
  <td class="stentry"> <p>Ensemble d’éléments comprenant des images simples, des visionneuses de vidéos, des visionneuses d’échantillons, des séries d’échantillons hiérarchiques, des visionneuses à 360°, des visionneuses à 360° bidimensionnelles, des visionneuses de pages et des fichiers vidéo. Chaque élément de visionneuse de supports peut également contenir une nuance facultative. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>visionneuse de vidéos </p></td> 
  <td class="stentry"> <p>Ensemble d’éléments constitué d’un de vidéos simples. </p></td> 
 </tr> 
</table>

## Détection du type d&#39;ensemble extérieur {#section-3dd6e453528d46898e559d31458a59ba}

Lorsqu’une `req=set` demande est reçue, le type de réponse à générer est déterminé par la valeur de `catalog::AssetType`. Si `catalog::AssetType` n’est pas défini, le type de réponse est déterminé par les règles suivantes :

* Si l’enregistrement se trouve dans le catalogue d’images ET `catalog::ImageSet` est défini

   * Supposons qu’un jeu de catalogues électroniques soit défini si au moins une entrée du champ Imageset d’enregistrement contient un deux-points
   * Supposons qu’un jeu de supports comporte au moins deux points-virgules dans le champ Imageset de l’enregistrement.
   * Supposons qu’une visionneuse d’images contienne au moins un point-virgule dans le champ Visionneuse d’images d’enregistrement.
   * Supposons qu’une visionneuse à 360° ne contienne pas de deux-points ou de points-virgules, mais qu’au moins une entrée contienne une visionneuse à 360° référencée ou une visionneuse en ligne (il s’agit d’une visionneuse à 360° 2D).
   * Supposons qu’un ensemble soit inconnu si aucune entrée ne contient deux points, un point-virgule, un ensemble référencé ou un ensemble en ligne (c’est-à-dire un d’images séparé par des virgules).

* Si l’enregistrement est trouvé dans les catalogues d’images ET de contenu statique

   * Supposons que l’extension de fichier se trouve dans l’ensemble suivant : mp3, mp4, flv, f4v, swf, xml
   * Impression d’une image autre

* Si l’enregistrement se trouve dans le catalogue de contenu statique mais PAS dans le catalogue d’images

   * Supposons que l’extension de fichier se trouve dans l’ensemble suivant : mp3, mp4, flv, f4v, swf, xml
   * Supposons que la statique soit utilisée autrement

* Si l’enregistrement est trouvé dans le catalogue d’images mais PAS dans le catalogue de contenu statique

   * Imaginer

* Si l’enregistrement n’est PAS trouvé dans le catalogue d’images et n’est PAS trouvé dans le catalogue de contenu statique

   * Supposons que l’extension de fichier soit basée sur des fichiers vidéo dans l’ensemble suivant : mp3, mp4, flv, f4v, swf, xml
   * Supposons qu’une image basée sur un fichier soit utilisée autrement

Dans tous les cas, la réponse XML résultante sera conforme au XML spécifié avec un noeud racine défini correspondant au type détecté.

## Détection du type d&#39;ensemble interne {#section-8f46490e467247e69ce284704def06f3}

Lorsque la visionneuse extérieure est détectée comme visionneuse de supports de type, la réponse contient un ensemble d&#39;éléments de visionneuse de supports correspondant à chaque entrée de visionneuse de supports dans `catalog::ImageSet`. Si le paramètre de type facultatif est spécifié pour une entrée de visionneuse de supports spécifique, il sera mappé à un type de sortie selon le tableau suivant :

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

Si le paramètre de type facultatif pour une entrée de visionneuse de supports spécifique n&#39;est pas spécifié ou correspond à un type non pris en charge, le type d&#39;élément de la visionneuse de supports est détecté automatiquement à l&#39;aide des mêmes règles que celles appliquées au niveau de l&#39;ensemble extérieur.

## Spécification XML {#section-c1bd60948ef545759a16885bb6fcc607}

La réponse xml renvoyée est conforme à la spécification suivante :

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

Le `labelkey=` modificateur est utilisé avec le `catalog::UserData`champ pour générer des libellés pour les images et les échantillons. Le `catalog:UserData` champ est analysé sous la forme d’un ensemble de paires clé/valeur et les index de la clé d’étiquette dans cet ensemble pour récupérer la valeur de la clé donnée. Cette valeur est ensuite renvoyée dans l’ *`l`* attribut pour le *`s`* et *`i`*.

## Restrictions appliquées {#section-b9f042873bee45a5ae11b69fd42f2bca}

Afin de limiter la taille de la réponse et d’éviter les problèmes d’auto-référence, la profondeur d’imbrication maximale est contrôlée par la propriété server `PS::fvctx.nestingLimit`. Si cette limite est dépassée, une erreur est renvoyée.

Afin de limiter la taille des réponses XML pour les jeux de catalogues électroniques volumineux, les métadonnées privées sont supprimées pour les éléments de jeu de brochures en fonction de la propriété server `PS::fvctx.brochureLimit`. Toutes les métadonnées privées associées à la brochure seront exportées jusqu’à ce que la limite de brochure soit atteinte. Une fois la limite dépassée, les cartes privées et les données utilisateur sont supprimées et un indicateur correspondant est défini pour indiquer le type de données supprimé.

Les visionneuses de supports imbriquées ne sont pas prises en charge. Une visionneuse de supports imbriquée est définie comme une visionneuse de supports contenant un élément d’ensemble de supports de type visionneuse de supports. Si cette condition est détectée, une erreur est renvoyée.

## Exemples {#section-588c9d33aa05482c86cd2b1936887228}

Pour obtenir des exemples de réponses XML pour une `req=set` requête, reportez-vous à la page Propriétés sous l’en-tête Exemples HTML.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Voir aussi {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), référence du catalogue [d’images](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)

