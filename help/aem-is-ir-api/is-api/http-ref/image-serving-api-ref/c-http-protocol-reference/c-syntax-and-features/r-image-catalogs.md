---
description: Les fonctionnalités et la syntaxe des catalogues d’images sont décrites dans cette section.
seo-description: Les fonctionnalités et la syntaxe des catalogues d’images sont décrites dans cette section.
seo-title: Catalogues d’images
solution: Experience Manager
title: Catalogues d’images
topic: Scene7 Image Serving - Image Rendering API
uuid: d329807a-22b0-42a3-9297-8dad7a1dce43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Catalogues d’images{#image-catalogs}

Les fonctionnalités et la syntaxe des catalogues d’images sont décrites dans cette section.

Les catalogues d’images   les fonctionnalités suivantes :

* Permet l’association permanente d’images avec certaines commandes de métadonnées et de modificateur.

   Les entrées des catalogues d’images sont référencées à l’aide d’une notation de raccourci ` *`rootId/objId`*`, où ` *`rootId`*` identifie le catalogue d’images et ` *`objId`*` identifie un enregistrement de données dans le catalogue.
* Indiquez les valeurs par défaut de certains attributs de requête, tels que la qualité JPEG ou l’application d’un filigrane.
* Gestion des polices, des  ICC, des définitions de macro et des modèles de requête

Même si aucun catalogue d’images spécifique n’est défini, toutes les fonctionnalités des catalogues d’images sont disponibles via le catalogue par défaut ( [!DNL default.ini]).

Si ` *`rootId`*` dans le chemin d’URL de la requête correspond `attribute::RootId` à un catalogue d’images spécifique, ce catalogue deviendra le catalogue principal de cette requête. Le catalogue principal fournit les attributs et paramètres par défaut pour l’ensemble de la requête. Si aucune correspondance n’est trouvée, le catalogue par défaut est utilisé à la place.

Un catalogue identifié dans une `src=` commande ou `mask=` fournit les attributs et données de catalogue suivants à la couche active :

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribut/Données</b> </th> 
   <th class="entry"> <b> Remarques</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribut:DefaultExt</span> </p> </td> 
   <td> <p> l’extension par défaut pour tous les chemins d’accès aux fichiers image dans le calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut:Expiration</span> </p> </td> 
   <td> <p> valeur par défaut pour <span class="codeph"> catalog::Expiration</span> ou expiration du calque actif si aucun enregistrement de catalogue n’est impliqué </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::Icc*</span> </p> </td> 
   <td> <p> le de couleurs ICC de travail, le mode de rendu et l’indicateur de compensation du point noir pour la requête et/ou le calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut:RootPath</span> </p> </td> 
   <td> <p> utilisé pour tous les chemins de fichier source du calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut:Resolution</span> </p> </td> 
   <td> <p> par défaut pour <span class="codeph"> le catalogue ::Résolution</span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::Ancre</span> </p> </td> 
   <td> <p> par défaut pour la <span class="codeph"> valeur anchor=</span> du calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::Expiration</span> </p> </td> 
   <td> <p> la plus petite valeur d’expiration de tous les calques est utilisée comme valeur de durée de vie de l’image de réponse. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue::IccProfile</span> </p> </td> 
   <td> <p> le de couleur de l’image source pour le calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::Carte</span> </p> </td> 
   <td> <p> les données de zone cliquable pour le calque actif ; </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::MaskPath</span> </p> </td> 
   <td> <p> par défaut pour <span class="codeph"> mask=</span> pour le calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue:Modificateur</span> </p> </td> 
   <td> <p> commandes de préfixe pour le calque actif (chaque commande du <span class="codeph"> catalogue::Modificateur</span> peut être remplacée par la même commande dans l’URL, si elle est spécifiée pour le même calque) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::Chemin</span> </p> </td> 
   <td> <p> le fichier image source du calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue::PostModificateur</span> </p> </td> 
   <td> <p> les commandes de suffixe pour le calque actif (similaires à <span class="codeph"> catalog::Modificateur</span>, mais les commandes dans <span class="codeph"> catalog::PostModificateur</span> remplacent les mêmes commandes spécifiées dans l’URL ou dans <span class="codeph"> le catalogue::Modificateur</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue::Résolution</span> </p> </td> 
   <td> <p> résolution d’objet du calque actif </p> </td> 
  </tr> 
 </tbody> 
</table>

Dans le même calque, `src=` et `mask=` doit faire référence au même catalogue d’images (le cas échéant).

Un catalogue identifié dans une `icc=` commande n’est utilisé que pour rechercher une entrée dans la table de ICC du catalogue. Aucun autre attribut ou donnée de catalogue n’est impliqué.

Si ` *`rootId`*` se résout dans un catalogue et que ` *`objId`*` correspond à un élément `catalog::Id` dans ce catalogue, ` *`rootId/objId`*` est remplacé par l’entrée de catalogue, un peu comme ceci :

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Voir aussi {#section-00e4f6b39cd14244bcce537a3f831259}

[Référence](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)du catalogue d’images, [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
