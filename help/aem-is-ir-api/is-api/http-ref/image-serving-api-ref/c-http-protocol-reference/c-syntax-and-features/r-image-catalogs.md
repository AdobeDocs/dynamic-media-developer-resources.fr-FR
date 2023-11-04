---
description: Les fonctionnalités et la syntaxe des catalogues d'images sont décrites dans cette section.
solution: Experience Manager
title: Catalogues d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# Catalogues d’images{#image-catalogs}

Les fonctionnalités et la syntaxe des catalogues d&#39;images sont décrites dans cette section.

Les catalogues d’images offrent les fonctionnalités suivantes :

* Autoriser l’association persistante des images avec certaines commandes de métadonnées et de modificateur.

  Les entrées des catalogues d’images sont référencées à l’aide d’une notation par raccourci. `*`rootId/objId`*`, où `*`rootId`*` identifie le catalogue d’images et `*`objId`*` identifie un enregistrement de données dans le catalogue.
* Indiquez les valeurs par défaut de certains attributs de requête, tels que la qualité du JPEG ou l’application d’un filigrane.
* Gestion des polices, des profils ICC, des définitions de macro et des modèles de requête

Même si aucun catalogue d’images spécifique n’est défini, toutes les fonctionnalités des catalogues d’images sont disponibles par le biais du catalogue par défaut ( [!DNL default.ini]).

If `*`rootId`*` dans les correspondances du chemin d’URL de la requête `attribute::RootId` d’un catalogue d’images spécifique, ce catalogue devient le catalogue principal de cette demande. Le catalogue principal fournit les attributs et paramètres par défaut pour l’ensemble de la requête. Si aucune correspondance n’est trouvée, le catalogue par défaut est utilisé à la place.

Un catalogue identifié dans un `src=` ou `mask=` fournit les attributs et données de catalogue suivants à la couche actuelle :

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribut/Données</b> </th> 
   <th class="entry"> <b> Remarques</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultExt</span> </p> </td> 
   <td> <p> l’extension par défaut pour tous les chemins d’accès aux fichiers image dans le calque actif ; </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> valeur par défaut <span class="codeph"> catalogue : Expiration</span> ou expiration du calque actif si aucun enregistrement de catalogue n’est impliqué </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Icc*</span> </p> </td> 
   <td> <p> le profil colorimétrique ICC de travail, l’intention de rendu et l’indicateur de compensation du point noir pour la demande et/ou le calque actif ; </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> utilisé pour tous les chemins d’accès aux fichiers source du calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
   <td> <p> valeur par défaut <span class="codeph"> catalogue : résolution</span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : Ancre</span> </p> </td> 
   <td> <p> valeur par défaut de la variable <span class="codeph"> anchor=</span> valeur du calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : Expiration</span> </p> </td> 
   <td> <p> la valeur d’expiration la plus petite de tous les calques est utilisée comme valeur de durée de vie de l’image de réponse. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : IccProfile</span> </p> </td> 
   <td> <p> le profil de couleur de l’image source pour le calque actif ; </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : Carte</span> </p> </td> 
   <td> <p> les données de zone cliquable pour le calque actif ; </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::MaskPath</span> </p> </td> 
   <td> <p> valeur par défaut <span class="codeph"> mask=</span> pour le calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : Modificateur</span> </p> </td> 
   <td> <p> commandes de préfixe pour le calque actif (chaque commande dans <span class="codeph"> catalogue : Modificateur</span> peut être remplacé par la même commande dans l’URL, si elle est spécifiée pour le même calque). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> le fichier image source pour le calque actif ; </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : PostModificateur</span> </p> </td> 
   <td> <p> commandes postfix pour le calque actif (similaires à <span class="codeph"> catalogue : Modificateur</span>, mais les commandes dans <span class="codeph"> catalogue : PostModificateur</span> remplacer les commandes spécifiées dans l’URL ou dans <span class="codeph"> catalogue : Modificateur</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : résolution</span> </p> </td> 
   <td> <p> Résolution de l’objet du calque actif </p> </td> 
  </tr> 
 </tbody> 
</table>

Dans la même couche, `src=` et `mask=` doit référencer le même catalogue d’images (le cas échéant).

Un catalogue identifié dans un `icc=` n’est utilisée que pour rechercher une entrée à partir de la table de profils ICC du catalogue. Aucun autre attribut ou donnée de catalogue n’est impliqué.

Si : `*`rootId`*` est résolu sur un catalogue, et `*`objId`*` est mis en correspondance avec un `catalog::Id` dans ce catalogue, puis `*`rootId/objId`*` est effectivement remplacé par l’entrée de catalogue de la manière suivante :

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Voir aussi {#section-00e4f6b39cd14244bcce537a3f831259}

[Référence du catalogue d’images](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
