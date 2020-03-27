---
description: Fichier matière. Indique les données de matériau, sous la forme d’une référence unique au catalogue de matériau, ou sous la forme d’un ou deux fichiers d’image ou de données de matériau, séparés par une virgule.
seo-description: Fichier matière. Indique les données de matériau, sous la forme d’une référence unique au catalogue de matériau, ou sous la forme d’un ou deux fichiers d’image ou de données de matériau, séparés par une virgule.
seo-title: src
solution: Experience Manager
title: src
topic: Scene7 Image Serving - Image Rendering API
uuid: 52751bcc-a65d-4441-a3b5-802d27b54b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# src{#src}

Fichier matière. Indique les données de matériau, sous la forme d’une référence unique au catalogue de matériau, ou sous la forme d’un ou deux fichiers d’image ou de données de matériau, séparés par une virgule.

`src = *``*|{{ *``*| *``*}[, *`catalogEntryMaterialFileEmbeddedReqMaterialFile`*]`

`srcE= *`nom`*`

`srcN= *`index`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> MaterialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> EmbeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">{'is{'<span class="varname"> isReq</span>'}}|{'ir{'<span class="varname"> irReq</span>'}'|{'{'<span class="varname"> ForeignReq</span>'}'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>ID de catalogue de matières (<span class="codeph"> attribut::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Entrée de catalogue de matières (<span class="codeph"> catalog::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>Fichier de style de matériau (<span class="filepath"> .vnc</span> ou <span class="filepath"> .vnw</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>Fichier de données image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>Demande de diffusion d’images. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>Rendu de la demande vers l’image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> étrangerReq</span> </p></td> 
  <td class="stentry"> <p>Demande à un serveur étranger. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nom</span> </p></td> 
  <td class="stentry"> <p>Nom d’une matière incorporée. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> index</span> </p></td> 
  <td class="stentry"> <p>Numéro d’index de base 0 pour un matériau incorporé. </p></td> 
 </tr> 
</table>

Les matériaux Texture, Décale et Papier peint répétables nécessitent une image unique, qui peut être spécifiée sous forme de fichier ou de requête incorporée.

Les documents d’armoire nécessitent un fichier de style d’armoire ( [!DNL .vnc]), qui ne peut pas être spécifié en tant que requête imbriquée. Un fichier d’image de texture est facultatif pour les armoires et, s’il est spécifié, il peut s’agir d’un fichier ou d’une requête incorporée.

Les matériaux de garnitures de fenêtre nécessitent un fichier de style de garnitures de fenêtre ( [!DNL .vnw]), qui ne peut pas être spécifié comme une requête imbriquée. Un fichier de texture est facultatif et, s’il est spécifié, il peut s’agir d’un fichier ou d’une requête incorporée.

Le rendu d’image utilise les mêmes règles que le service d’image pour rechercher des catalogues de matières, des entrées de catalogue et des fichiers de données. Pour plus d’informations, reportez-vous à la description du type de *`object`* données dans la documentation de la diffusion d’images.

*`materialFile`* est un chemin relatif à `attribute::RootPath`.

*`foreignReq`* peut être soit une URL relative à `attribute::RootUrl`, soit une URL absolue si `attribute::AllowDirectUrls` est définie.

Si *`catId`* n’est pas spécifié, le catalogue de sessions est utilisé.

`srcE=` et `srcN=` donner accès aux matériaux incorporés dans la vignette.

## Formats de fichiers pris en charge {#section-f2186d3eef834fc8bbecb2bc68daacad}

Le rendu d’image prend en charge les mêmes formats d’image source que Scene7 Image Serving.

Les applications qui nécessitent des données d’image dans plusieurs résolutions différentes sont plus performantes lors de l’utilisation du format PTIFF (Scene7 pyramid TIFF) à plusieurs résolutions. Image Serving inclut l’utilitaire Image Converter (IC) qui crée des images PTIFF à partir de n’importe quel format pris en charge.

Reportez-vous à la description de l’utilitaire IC dans la documentation de Image Serving pour obtenir un complet des formats de fichiers pris en charge.

## Propriétés {#section-e68d03788d534e2184147987d51dfd0f}

Attribut de matière. Obligatoire pour tous les matériaux, à l&#39;exception de la couleur unie (non autorisée pour les matériaux de couleur unie). Toutes les chaînes sont sensibles à la casse. *`index`* doit être supérieur ou égal à 0.

## Par défaut {#section-dde549c1917540dc8f9555962202da3c}

Aucune

## Exemple {#section-675865444f8a4d35b9fc6e58b36e3438}

Un MSS pour une armoire colorée avec une texture répétable distincte:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

Le même matériau peut être situé dans un catalogue de matières `'cat`&quot;au dossier `12-3-2`&quot;:

`…&obj=cabinets&src=cat/12-3-2&…`

Demande imbriquée au serveur d’images pour obtenir une image de texture :

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Voir aussi {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Catalogues](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)matières, [attribut::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402), [attribut::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
