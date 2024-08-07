---
title: modèle
description: Modèle de composition. Permet de spécifier un modèle de composition situé dans un catalogue autre que le catalogue principal.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 4%

---

# modèle{#template}

Modèle de composition. Permet de spécifier un modèle de composition dans un catalogue autre que le catalogue principal.

`template= *`template`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> objet</span> </p> </td> 
  <td class="stentry"> <p>Modèle. </p></td> 
 </tr> 
</table>

*`template`* doit être une entrée de catalogue d’images avec le corps de modèle contenu dans `catalog::Modifier`.

Lorsque `template=` est présent, l’objet spécifié dans le chemin de requête n’est pas appliqué en tant que source pour le calque 0. Cependant, il peut être référencé en tant que `src=` ou `mask=` n’importe où dans le modèle en utilisant la variable de chemin prédéfinie `$object$` comme valeur `src=`. `catalog::Modifier` de l’objet spécifié dans le chemin de requête n’est appliqué qu’avec la substitution de `$object$` dans le modèle, tandis que `catalog::PostModifier` est toujours appliqué.

Le calque 0 est défini dans le corps du modèle et peut être une image, une couleur unie, du texte ou une couche de requête imbriquée ou incorporée.

`catalog:PostModifier` de *`object`* est ignoré lorsque *`object`* est utilisé avec `template=`.

## Par défaut {#section-9de53ea27c4b4fd4811e40e345d8ba05}

Aucune

## Propriétés {#section-daf3afb1d09c45a6a394468d0874c439}

Attribut de requête. S’applique quel que soit le paramètre de calque actif.

## Exemple {#section-9a4f260ed43342b186b0fe855f34bca6}

Voir les exemples dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-067587444f774469931ecafd5a39834c}

[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Variable de chemin prédéfinie](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
