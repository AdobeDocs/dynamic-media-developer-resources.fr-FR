---
description: Les fonctionnalités et la syntaxe des catalogues d’images sont décrites dans cette section.
solution: Experience Manager
title: Catalogues d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---


# Catalogues d’images{#image-catalogs}

Les fonctionnalités et la syntaxe des catalogues d’images sont décrites dans cette section.

Les catalogues d’images offre les fonctionnalités suivantes :

* Permet l’association permanente d’images à l’aide de certaines commandes de métadonnées et de modificateur.

   Les entrées des catalogues d’images sont référencées à l’aide d’une notation de raccourci `*`rootId/objId`*`, où `*`rootId`*` identifie le catalogue d’images et `*`objId`*` identifie un enregistrement de données dans le catalogue.
* Indiquez les valeurs par défaut de certains attributs de requête, tels que la qualité JPEG ou si un filigrane doit être appliqué.
* Gérer les polices, les profils ICC, les définitions de macro et les modèles de demande

Même si aucun catalogue d’images spécifique n’est défini, toutes les fonctionnalités des catalogues d’images sont disponibles par le biais du catalogue par défaut ( [!DNL default.ini]).

Si `*`rootId`*` dans le chemin d’URL de la requête correspond à `attribute::RootId` d’un catalogue d’images spécifique, ce catalogue deviendra le catalogue principal de cette requête. Le catalogue principal fournit les attributs et les paramètres par défaut pour l’ensemble de la requête. Si aucune correspondance n’est trouvée, le catalogue par défaut est utilisé à la place.

Un catalogue identifié dans une commande `src=` ou `mask=` fournit les attributs et données de catalogue suivants à la couche actuelle :

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribut/Données</b> </th> 
   <th class="entry"> <b> Remarques</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::DefaultExt</span> </p> </td> 
   <td> <p> l’extension par défaut pour tous les chemins de fichier image dans le calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::Expiration</span> </p> </td> 
   <td> <p> valeur par défaut pour <span class="codeph"> catalog::Expiration</span> ou expiration du calque actif si aucun enregistrement de catalogue n'est impliqué </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::Icc*</span> </p> </td> 
   <td> <p> l’indicateur de compensation du profil de couleur ICC de travail, de l’intention de rendu et du point noir pour la demande et/ou le calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::RootPath</span> </p> </td> 
   <td> <p> utilisé pour tous les chemins de fichier source du calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::Résolution</span> </p> </td> 
   <td> <p> valeur par défaut pour <span class="codeph"> catalog::Resolution</span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : Ancre</span> </p> </td> 
   <td> <p> valeur par défaut de la valeur <span class="codeph"> anchor=</span> du calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::Expiration</span> </p> </td> 
   <td> <p> la plus petite valeur d’expiration de tous les calques est utilisée comme valeur de durée de vie de l’image de réponse. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::IccProfile</span> </p> </td> 
   <td> <p> profil de couleur de l’image source pour le calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::Carte</span> </p> </td> 
   <td> <p> les données de zone cliquable pour le calque actif ; </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::MaskPath</span> </p> </td> 
   <td> <p> valeur par défaut de <span class="codeph"> mask=</span> pour le calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : Modificateur</span> </p> </td> 
   <td> <p> les commandes de préfixe pour le calque actif (chaque commande de <span class="codeph"> catalog::Modificateur</span> peut être remplacée par la même commande dans l'URL, si elle est spécifiée pour le même calque). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : chemin</span> </p> </td> 
   <td> <p> le fichier image source pour le calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::PostModificateur</span> </p> </td> 
   <td> <p> les commandes postfix pour le calque actif (semblables à <span class="codeph"> catalog::Modificateur</span>, mais les commandes de <span class="codeph"> catalog::PostModificateur</span> remplacent les mêmes commandes spécifiées dans l'URL ou dans le <span class="codeph"> catalogue::Modificateur</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : résolution</span> </p> </td> 
   <td> <p> résolution d’objet du calque actif </p> </td> 
  </tr> 
 </tbody> 
</table>

Dans le même calque, `src=` et `mask=` doivent référencer le même catalogue d’images (le cas échéant).

Un catalogue identifié dans une commande `icc=` n&#39;est utilisé que pour rechercher une entrée dans la table de profil ICC du catalogue. Aucun autre attribut ou donnée de catalogue n’est impliqué.

Si `*`rootId`*` correspond à un catalogue et que `*`objId`*` correspond à `catalog::Id` dans ce catalogue, `*`rootId/objId`*` est effectivement remplacé par l&#39;entrée de catalogue de la manière suivante :

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Voir aussi {#section-00e4f6b39cd14244bcce537a3f831259}

[Référence](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) du catalogue d’images,  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
