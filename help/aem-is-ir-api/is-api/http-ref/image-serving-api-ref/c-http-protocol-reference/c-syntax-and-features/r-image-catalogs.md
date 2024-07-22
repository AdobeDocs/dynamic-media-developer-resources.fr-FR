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

  Les entrées dans les catalogues d’images sont référencées à l’aide d’une notation de raccourci `*`rootId/objId`*`, où `*`rootId`*` identifie le catalogue d’images et `*`objId`*` identifie un enregistrement de données dans le catalogue.
* Indiquez les valeurs par défaut de certains attributs de requête, tels que la qualité du JPEG ou l’application d’un filigrane.
* Gestion des polices, des profils ICC, des définitions de macro et des modèles de requête

Même si aucun catalogue d’images spécifique n’est défini, toutes les fonctionnalités des catalogues d’images sont disponibles par le biais du catalogue par défaut ( [!DNL default.ini]).

Si `*`rootId`*` dans le chemin d’URL de la requête correspond à `attribute::RootId` d’un catalogue d’images spécifique, ce catalogue devient le catalogue principal de cette requête. Le catalogue principal fournit les attributs et paramètres par défaut pour l’ensemble de la requête. Si aucune correspondance n’est trouvée, le catalogue par défaut est utilisé à la place.

Un catalogue identifié dans une commande `src=` ou `mask=` fournit les attributs et données de catalogue suivants à la couche actuelle :

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribute/Data</b> </th> 
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
   <td> <p> valeur par défaut de <span class="codeph"> catalog::Expiration</span> ou expiration de la couche actuelle si aucun enregistrement de catalogue n’est impliqué </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attribut <span class="codeph"> ::Icc*</span> </p> </td> 
   <td> <p> le profil colorimétrique ICC de travail, l’intention de rendu et l’indicateur de compensation du point noir pour la demande et/ou le calque actif ; </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> utilisé pour tous les chemins d’accès aux fichiers source du calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
   <td> <p> Par défaut pour le catalogue <span class="codeph"> ::Resolution</span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> </p> </td> 
   <td> <p> valeur par défaut pour la valeur <span class="codeph"> anchor=</span> du calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Catalogue <span class="codeph"> ::Expiration</span> </p> </td> 
   <td> <p> la valeur d’expiration la plus petite de tous les calques est utilisée comme valeur de durée de vie de l’image de réponse. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Catalogue <span class="codeph"> ::IccProfile</span> </p> </td> 
   <td> <p> le profil de couleur de l’image source pour le calque actif ; </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Catalogue <span class="codeph"> ::Map</span> </p> </td> 
   <td> <p> les données de zone cliquable pour le calque actif ; </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> valeur par défaut de <span class="codeph"> mask=</span> pour le calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Catalogue <span class="codeph"> ::Modifier</span> </p> </td> 
   <td> <p> les commandes de préfixe pour le calque actif (chaque commande du catalogue <span class="codeph"> ::Modifier</span> peut être remplacée par la même commande de l’URL, si elle est spécifiée pour le même calque). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Catalogue <span class="codeph"> ::Path</span> </p> </td> 
   <td> <p> le fichier image source pour le calque actif ; </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Catalogue <span class="codeph"> ::PostModifier</span> </p> </td> 
   <td> <p> les commandes postfix pour la couche actuelle (similaires au catalogue <span class="codeph"> ::Modifier</span>, mais les commandes du catalogue <span class="codeph"> ::PostModifier</span> remplacent les mêmes commandes spécifiées dans l’URL ou dans le catalogue <span class="codeph"> ::Modifier</span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Catalogue <span class="codeph"> ::Resolution</span> </p> </td> 
   <td> <p> Résolution de l’objet du calque actif </p> </td> 
  </tr> 
 </tbody> 
</table>

Dans la même couche, `src=` et `mask=` doivent référencer le même catalogue d’images (le cas échéant).

Un catalogue identifié dans une commande `icc=` n’est utilisé que pour rechercher une entrée de la table de profils ICC du catalogue. Aucun autre attribut ou donnée de catalogue n’est impliqué.

Si `*`rootId`*` correspond à un catalogue et que `*`objId`*` correspond à un `catalog::Id` dans ce catalogue, alors `*`rootId/objId`*` est remplacé de manière efficace par l’entrée de catalogue un peu comme ceci :

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Voir aussi {#section-00e4f6b39cd14244bcce537a3f831259}

[Référence du catalogue d’images](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
