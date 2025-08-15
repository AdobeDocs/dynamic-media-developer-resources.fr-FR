---
description: Spécificateur d’objet Source. Les objets de profil Image, SVG et ICC peuvent être spécifiés sous la forme d’entrées de catalogue d’images ou de chemins d’accès de fichiers relatifs
solution: Experience Manager
title: objet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# objet{#object}

Spécificateur d’objet Source. Les objets de profil Image, SVG et ICC peuvent être spécifiés sous la forme d’entrées de catalogue d’images ou de chemins d’accès de fichiers relatifs

`*`object`*[/]{[ *`rootId`*/] *`objId`*}| *`path`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>nom du catalogue d’images (attribut <span class="codeph"> : RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId </span> </span> </p> </td> 
  <td class="stentry"> <p>ID de l’enregistrement de profil d’image, de SVG, de modèle ou ICC dans le catalogue d’images principal, par défaut ou spécifié </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> chemin <span class="varname">’accès </span> </span> </p> </td> 
  <td class="stentry"> <p>Nom et chemin d’accès du fichier de profil ICC, masque ou image relative </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> objet <span class="varname"> </span> </span> </p> </td> 
  <td class="stentry"> <p>peut se produire dans le chemin d’URL principal ou dans une commande <span class="codeph"> src= </span>, <span class="codeph"> mask= </span> ou <span class="codeph"> icc= </span> </p> </td> 
 </tr> 
</table>

*`rootId`* identifie un catalogue d’images. (Voir [Catalogue d’images](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) pour plus d’informations.) Si *`rootId`* est spécifié dans le chemin d’accès à l’URL, ce catalogue devient le *catalogue principal* de cette requête. Sinon, le catalogue par défaut est utilisé comme catalogue principal. Plusieurs catalogues d’images différents peuvent être utilisés dans la même requête.

Le serveur suppose initialement que *`rootId`* est omis dans les commandes `src=`, `mask=` et `icc=` et tente de trouver une entrée de catalogue dans le catalogue principal. En fait, le serveur tente d’utiliser toute la chaîne de *`object`* comme *`objId.`*

Si une entrée de catalogue est trouvée, elle est utilisée ; sinon, le serveur tente ensuite de correspondre à la *`rootId`* d’un catalogue d’images. Si un catalogue est identifié, il est recherché *`objId`*. Si une entrée est trouvée, elle est utilisée.

Dans le cas contraire, *`object`* est supposé être un chemin d’accès au fichier explicite. Dans ce cas, si `attribute::FullMatch` est défini dans le catalogue principal, le catalogue est ignoré pour cet objet et le catalogue par défaut est utilisé à la place. Si `attribute::FullMatch` n’est pas défini, le catalogue principal est utilisé pour un traitement ultérieur.

*`rootId`* et *`objId`* respectent la casse. *`path`* est sensible à la casse uniquement sous UNIX.

Si un `/` de début est spécifié, la recherche porte sur le catalogue par défaut et non sur le catalogue principal. Cela s’avère principalement utile lorsqu’un chemin d’accès explicite nécessite `default::RootPath` plutôt que l’`attribute::RootPath` du catalogue principal, mais peut également être utilisé pour accéder à des entrées du catalogue par défaut qui seraient sinon remplacées par des entrées du catalogue principal.

Reportez-vous à *Gestion du contenu* dans le *Guide de configuration du serveur* pour plus d’informations sur la traduction de l’*`path`* en chemin d’accès physique au fichier.

>[!NOTE]
>
>Les caractères &#39;,&#39; ne sont pas autorisés dans *`object.`*

## Formats de fichiers image pris en charge {#section-12c85aead78e4f759856ca9ff10637d7}

Reportez-vous à la description de l&#39;utilitaire IC (Image Converter) pour une liste complète des formats de fichiers pris en charge.

Les applications qui nécessitent des données d’image dans plusieurs résolutions différentes fonctionnent mieux avec le format PTIF (Dynamic Media pyramid TIFF) à plusieurs résolutions. L’utilitaire IC permet de créer des images PTIF à partir de n’importe quel format d’image pris en charge.

## Exemples {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Accès à une image et à un profil ICC dans deux catalogues d’images différents**

Récupérez l’image « [!DNL myImage] » dans le catalogue d’images identifié comme « [!DNL myCatalog] » et joignez le profil ICC « [!DNL sRGB] » situé dans le catalogue d’images nommé « [!DNL myProfiles] » :

` http:// *`serveur`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Utilisation d’un seul catalogue d’images avec superposition

**Créez une image composite simple composée de trois calques, tous récupérés depuis « [!DNL myCatalog] » :**

` http:// *`serveur`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Accès direct aux fichiers image tout en utilisant un catalogue pour fournir des attributs**

Accédez aux [!DNL my/image/path/myImage.tif] à l’aide des attributs jpg par défaut configurés dans `myImageCatalog` :

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Voir aussi {#section-b6eccefad63f441d922699c4aba58fc9}

[Utilitaire IC](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
