---
description: Spécificateur d’objet source. Les objets Image, SVG et ICC  peuvent être spécifiés sous forme d’entrées de catalogue d’images ou de chemins de fichier relatifs.
seo-description: Spécificateur d’objet source. Les objets Image, SVG et ICC  peuvent être spécifiés sous forme d’entrées de catalogue d’images ou de chemins de fichier relatifs.
seo-title: objet
solution: Experience Manager
title: objet
topic: Scene7 Image Serving - Image Rendering API
uuid: 8d25b47d-0f23-4d9a-a7e6-6e865ae4114e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# objet{#object}

Spécificateur d’objet source. Les objets Image, SVG et ICC  peuvent être spécifiés sous forme d’entrées de catalogue d’images ou de chemins de fichier relatifs.

` *``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span></span> </p> </td> 
  <td class="stentry"> <p>nom du catalogue d’images ( <span class="codeph"> attribut::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId </span></span> </p> </td> 
  <td class="stentry"> <p>ID de l’enregistrement de l’image, du SVG, du modèle ou du ICC dans le catalogue d’images spécifié, principal ou par défaut </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> chemin </span></span> </p> </td> 
  <td class="stentry"> <p>image relative, masque ou chemin d’accès et nom  fichier ICC </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> , objet </span></span> </p> </td> 
  <td class="stentry"> <p>peut se produire soit dans le chemin d’accès de l’URL principale, soit dans une commande <span class="codeph"> src= </span>, <span class="codeph"> mask= </span>ou <span class="codeph"> icc= </span> . </p> </td> 
 </tr> 
</table>

*`rootId`* identifie un catalogue d’images. (See [Image Catalog](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) for details.) Si *`rootId`* est spécifié dans le chemin d’accès de l’URL, ce catalogue devient le catalogue ** principal de cette requête. Sinon, le catalogue par défaut est utilisé comme catalogue principal. Plusieurs catalogues d’images différents peuvent être utilisés dans la même requête.

Le serveur suppose au départ que *`rootId`* les commandes `src=`, `mask=`et `icc=` sont omises et qu’il tente de trouver une entrée de catalogue dans le catalogue principal. En fait, le serveur tente d’utiliser la *`object`* chaîne entière comme *`objId.`*

Si une entrée de catalogue est trouvée, elle est utilisée ; dans le cas contraire, le serveur tente ensuite de faire correspondre le catalogue *`rootId`* d’images. Si un catalogue est identifié, il est recherché *`objId`*. Si et entrée est trouvée, elle est utilisée.

Dans le cas contraire, *`object`* il s’agit d’un chemin de fichier explicite. Dans ce cas, si `attribute::FullMatch` est défini dans le catalogue principal, le catalogue est ignoré pour cet objet et le catalogue par défaut est utilisé à la place. Si `attribute::FullMatch` n’est pas défini, le catalogue principal est utilisé pour un traitement ultérieur.

Les deux *`rootId`* et *`objId`* sont sensibles à la casse. *`path`* est sensible à la casse sous UNIX uniquement.

Si un caractère &quot;/&quot; de début est spécifié, le catalogue par défaut est recherché à la place du catalogue principal. Cela s’avère particulièrement utile lorsqu’un chemin explicite nécessite `default::RootPath` plutôt que celui du catalogue principal `attribute::RootPath`, mais peut également être utilisé pour accéder aux entrées du catalogue par défaut qui seraient sinon remplacées par les entrées du catalogue principal.

Consultez *Gestion du contenu* dans le Guide *de configuration du* serveur pour plus d’informations sur la manière dont *`path`* est traduit en chemin de fichier physique.

>[!NOTE]
>
>La virgule &quot;,&quot; ne peut pas contenir de caractères *`object.`*

## Formats de fichier image pris en charge {#section-12c85aead78e4f759856ca9ff10637d7}

Reportez-vous à la description de l’utilitaire IC (Image Converter) pour obtenir un complet des formats de fichiers pris en charge.

Les applications qui nécessitent des données d’image dans plusieurs résolutions différentes sont plus performantes lors de l’utilisation du format PTIF (Scene7 pyramid TIFF). L’utilitaire IC est utilisé pour créer des images PTIF à partir de n’importe quel format d’image pris en charge.

## Exemples {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Accès à une image et à un ICC dans deux catalogues d’images différents**

Récupérez l’image &#39; [!DNL myImage]&#39; dans le catalogue d’images identifié comme &#39; [!DNL myCatalog]&#39; et joignez le ICC &#39; [!DNL sRGB]&#39; situé dans le catalogue d’images nommé &#39; [!DNL myProfiles]&#39; :

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Utilisation d’un catalogue d’images unique avec calques

**Créez une image composite simple composée de trois calques, tous récupérés à partir de &quot;[!DNL myCatalog]&quot; :**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Accès direct aux fichiers d’image tout en continuant à utiliser un catalogue pour fournir des attributs**

Accès [!DNL my/image/path/myImage.tif], à l’aide des attributs jpg par défaut configurés dans `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Voir aussi {#section-b6eccefad63f441d922699c4aba58fc9}

[Utilitaire](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)IC, [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribut::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
