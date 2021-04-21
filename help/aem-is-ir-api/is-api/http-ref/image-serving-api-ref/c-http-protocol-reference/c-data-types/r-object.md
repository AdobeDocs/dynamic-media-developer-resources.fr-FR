---
description: Spécificateur d’objet source. Les objets Image, SVG et profil ICC peuvent être spécifiés en tant qu’entrées de catalogue d’images ou chemins d’accès aux fichiers relatifs.
solution: Experience Manager
title: objet
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 1%

---


# objet{#object}

Spécificateur d’objet source. Les objets Image, SVG et profil ICC peuvent être spécifiés en tant qu’entrées de catalogue d’images ou chemins d’accès aux fichiers relatifs.

`*``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId  </span> </span> </p> </td> 
  <td class="stentry"> <p>nom du catalogue d’images ( <span class="codeph"> attribut::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID de l’enregistrement d’image, SVG, de modèle ou de profil ICC dans le catalogue d’images principal, par défaut ou spécifié </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> chemin  </span> </span> </p> </td> 
  <td class="stentry"> <p>chemin d’accès et nom du fichier d’image, de masque ou de profil ICC relatif </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objet  </span> </span> </p> </td> 
  <td class="stentry"> <p>peut se produire soit dans le chemin d’accès de l’URL principale, soit dans une commande <span class="codeph"> src= </span>, <span class="codeph"> mask= </span>, soit <span class="codeph"> icc= </span> </p> </td> 
 </tr> 
</table>

*`rootId`* identifie un catalogue d’images. (Voir [Catalogue d’images](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) pour plus de détails.) Si *`rootId`* est spécifié dans le chemin d’accès de l’URL, ce catalogue devient le *catalogue principal* pour cette demande. Sinon, le catalogue par défaut est utilisé comme catalogue principal. Plusieurs catalogues d’images différents peuvent être utilisés dans la même requête.

Le serveur suppose initialement que *`rootId`* est omis dans les commandes `src=`, `mask=` et `icc=` et qu&#39;il tente de trouver une entrée de catalogue dans le catalogue principal. En fait, le serveur tente d’utiliser la chaîne *`object`* complète sous la forme *`objId.`*.

Si une entrée de catalogue est trouvée, elle est utilisée ; dans le cas contraire, le serveur tente ensuite de faire correspondre le *`rootId`* d’un catalogue d’images. Si un catalogue est identifié, il est recherché *`objId`*. Si une entrée est trouvée, elle est utilisée.

Dans le cas contraire, *`object`* est supposé être un chemin de fichier explicite. Dans ce cas, si `attribute::FullMatch` est défini dans le catalogue principal, le catalogue est ignoré pour cet objet et le catalogue par défaut est utilisé à la place. Si `attribute::FullMatch` n&#39;est pas défini, le catalogue principal est utilisé pour un traitement ultérieur.

*`rootId`* et *`objId`* sont tous deux sensibles à la casse. *`path`* est sensible à la casse sous UNIX uniquement.

Si un caractère de début &quot;/&quot; est spécifié, le catalogue par défaut est recherché à la place du catalogue principal. Cela est d&#39;abord utile lorsqu&#39;un chemin explicite nécessite `default::RootPath` plutôt que `attribute::RootPath` du catalogue principal, mais peut également être utilisé pour accéder aux entrées du catalogue par défaut qui seraient sinon remplacées par les entrées du catalogue principal.

Consultez *Gestion du contenu* dans le *Guide de configuration du serveur* pour plus d&#39;informations sur la façon dont *`path`* est traduit en chemin de fichier physique.

>[!NOTE]
>
>La virgule &quot;,&quot; caractères n&#39;est pas autorisée dans *`object.`*

## Formats de fichier image pris en charge {#section-12c85aead78e4f759856ca9ff10637d7}

Reportez-vous à la description de l’utilitaire IC (Image Converter) pour obtenir une liste complète des formats de fichiers pris en charge.

Les applications qui nécessitent des données d’image dans plusieurs résolutions différentes seront plus performantes lors de l’utilisation du format de résolution multiple de la pyramide Dynamic Media TIFF (PTIF). L’utilitaire IC est utilisé pour créer des images PTIF à partir de n’importe quel format d’image pris en charge.

## Exemples {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Accès à une image et à un profil ICC dans deux catalogues d’images différents**

Récupérez l’image &quot; [!DNL myImage]&quot; dans le catalogue d’images identifié comme &quot; [!DNL myCatalog]&quot; et joignez le profil ICC &quot; [!DNL sRGB]&quot; situé dans le catalogue d’images nommé &quot; [!DNL myProfiles]&quot; :

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Utilisation d’un catalogue d’images unique avec couche

**Créez une image composite simple composée de trois couches, toutes récupérées à partir de &quot;  [!DNL myCatalog]&quot; :**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Accès direct aux fichiers image tout en utilisant un catalogue pour fournir des attributs**

Accédez à [!DNL my/image/path/myImage.tif] à l’aide des attributs jpg par défaut configurés dans `myImageCatalog` :

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Voir aussi {#section-b6eccefad63f441d922699c4aba58fc9}

[Utilitaire](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b) IC,  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
