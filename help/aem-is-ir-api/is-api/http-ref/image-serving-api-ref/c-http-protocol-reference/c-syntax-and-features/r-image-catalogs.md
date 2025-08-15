---
description: Les fonctionnalités et la syntaxe des catalogues d’images sont décrites dans cette section.
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

Les fonctionnalités et la syntaxe des catalogues d’images sont décrites dans cette section.

Les catalogues d’images offrent les fonctionnalités suivantes :

* Autoriser l’association persistante des images à certaines métadonnées et commandes de modification.

  Les entrées des catalogues d’images sont référencées à l’aide d’une notation de raccourci `*`rootId/objId`*`, où `*`rootId`*` identifie le catalogue d’images et `*`objId`*` identifie un enregistrement de données dans le catalogue.
* Fournissez des valeurs par défaut pour certains attributs de requête, tels que la qualité du JPEG ou si un filigrane doit être appliqué.
* Gérer les polices, les profils ICC, les définitions de macro et les modèles de requête

Même si aucun catalogue d’images spécifique n’est défini, toutes les fonctionnalités des catalogues d’images sont disponibles par le biais du catalogue par défaut ( [!DNL default.ini]).

Si `*`rootId`*` dans le chemin d’accès URL de la requête correspond à l’`attribute::RootId` d’un catalogue d’images spécifique, ce catalogue devient le catalogue principal de cette requête. Le catalogue principal fournit les attributs et paramètres par défaut pour l’ensemble de la requête. Si aucune correspondance n’est trouvée, le catalogue par défaut est utilisé à la place.

Un catalogue identifié dans une commande `src=` ou `mask=` fournit les attributs de catalogue et les données suivants à la couche active :

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribut/Données</b> </th> 
   <th class="entry"> <b> notes</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultExt</span> </p> </td> 
   <td> <p> l’extension par défaut pour tous les chemins d’accès aux fichiers image du calque actuel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> Valeur par défaut pour <span class="codeph"> catalogue::Expiration</span> ou expiration du calque actif si aucun enregistrement de catalogue n’est impliqué </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Icc*</span> </p> </td> 
   <td> <p> le profil colorimétrique ICC fonctionnel, l’intention de rendu et l’indicateur de compensation de point noir pour la requête et/ou le calque actuel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> utilisé pour tous les chemins d’accès aux fichiers sources du calque actuel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
   <td> <p> par défaut pour <span class="codeph"> catalogue::Resolution</span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> </p> </td> 
   <td> <p> valeur par défaut de la <span class="codeph"> anchor=</span> du calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> </p> </td> 
   <td> <p> la plus petite valeur d’expiration de tous les calques est utilisée comme valeur de durée de vie de l’image de réponse </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::IccProfile</span> </p> </td> 
   <td> <p> profil colorimétrique de l’image source du calque actuel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map</span> </p> </td> 
   <td> <p> données de la zone cliquable pour le calque actuel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> par défaut pour <span class="codeph"> masque=</span> pour le calque actif </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> </p> </td> 
   <td> <p> commandes de préfixe pour le calque actuel (chaque commande <span class="codeph"> catalog::Modifier</span> peut être remplacée par la même commande dans l’URL, si elle est spécifiée pour le même calque) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> fichier image source du calque actuel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::PostModifier</span> </p> </td> 
   <td> <p> les commandes de suffixe pour le calque actuel (similaires à <span class="codeph"> catalog::Modifier</span>, mais les commandes de <span class="codeph"> catalog::PostModifier</span> remplacent les mêmes commandes spécifiées dans l’URL ou dans <span class="codeph"> catalog::Modifier</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> </p> </td> 
   <td> <p> résolution objet du calque actif </p> </td> 
  </tr> 
 </tbody> 
</table>

Dans le même calque, `src=` et `mask=` doivent référencer le même catalogue d’images (le cas échéant).

Un catalogue identifié dans une commande `icc=` est utilisé uniquement pour rechercher une entrée dans la table de profils ICC du catalogue. Aucun autre attribut ou donnée de catalogue n’est impliqué.

Si, `*`rootId`*` est résolu sur un catalogue et que `*`objId`*` est mis en correspondance avec un `catalog::Id` de ce catalogue, `*`rootId/objId`*` est effectivement remplacé par l’entrée de catalogue un peu comme suit :

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Voir aussi {#section-00e4f6b39cd14244bcce537a3f831259}

[Référence du catalogue d’images](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
