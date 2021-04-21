---
description: Fichier matière. Spécifie les données de matériau, sous la forme d'une référence de catalogue de matériau unique, ou sous la forme d'un ou deux fichiers d'image ou de données de matériau, séparés par une virgule.
solution: Experience Manager
title: src
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 2%

---


# src{#src}

Fichier matière. Spécifie les données de matériau, sous la forme d&#39;une référence de catalogue de matériau unique, ou sous la forme d&#39;un ou deux fichiers d&#39;image ou de données de matériau, séparés par une virgule.

`src = *``*|{{ *``*| *``*}[, *`catalogEntryMaterialFileEmbeddedReqMaterialFile`*]`

`srcE= *`name`*`

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
  <td class="stentry"> <p><span class="varname"> imbriquéReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;lacer ;'is&amp;accolade ;'<span class="varname"> isReq</span>'&amp;accolade ;'&amp;accolade ;|&amp;accolade ;'ir&amp;accolade ;'<span class="varname"> irReq</span>'&amp;accolade ;'|&amp;accolade ;'&amp;accolade ;'<span class="varname"> étrangerReq</span>'&amp;accolade ;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>ID catalogue de matières (<span class="codeph"> attribut::RootId</span>). </p></td> 
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
  <td class="stentry"> <p>Demande de rendu d’image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>Demande à un serveur étranger. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p></td> 
  <td class="stentry"> <p>Nom d'un matériau incorporé. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> index</span> </p></td> 
  <td class="stentry"> <p>Numéro d'index de base 0 pour un matériau incorporé. </p></td> 
 </tr> 
</table>

Les matériaux Texture, Décale et Papier peint répétables nécessitent une seule image, qui peut être spécifiée sous la forme d’un fichier ou d’une requête incorporée.

Les documents d&#39;armoire nécessitent un fichier de style d&#39;armoire ( [!DNL .vnc]), qui ne peut pas être spécifié comme une requête imbriquée. Un fichier image de texture est facultatif pour les armoires et, s&#39;il est spécifié, il peut s&#39;agir d&#39;un fichier ou d&#39;une requête incorporée.

Les matériaux de garnitures de fenêtre nécessitent un fichier de style de garnitures de fenêtre ( [!DNL .vnw]), qui ne peut pas être spécifié comme une requête imbriquée. Un fichier de texture est facultatif et, s’il est spécifié, il peut s’agir d’un fichier ou d’une requête incorporée.

Le rendu d’images utilise les mêmes règles que le traitement d’images pour rechercher des catalogues de matières, des entrées de catalogue et des fichiers de données. Pour plus d’informations, reportez-vous à la description du type de données *`object`* dans la documentation de la diffusion d’images.

*`materialFile`* est un chemin relatif par rapport à  `attribute::RootPath`.

*`foreignReq`* peut être une URL relative à  `attribute::RootUrl`ou une URL absolue si  `attribute::AllowDirectUrls` elle est définie.

Si *`catId`* n&#39;est pas spécifié, le catalogue de sessions est utilisé.

`srcE=` et  `srcN=` permettent d&#39;accéder aux matériaux incorporés dans la vignette.

## Formats de fichiers pris en charge {#section-f2186d3eef834fc8bbecb2bc68daacad}

Le rendu d’images prend en charge les mêmes formats d’image source que le service d’images Dynamic Media.

Les applications qui nécessitent des données d’image de plusieurs résolutions différentes seront plus performantes lors de l’utilisation du format de résolution multiple TIFF (PTIFF) de la pyramide Scene7. Image Serving inclut l’utilitaire Image Converter (IC) qui crée des images PTIFF à partir de n’importe quel format pris en charge.

Pour obtenir une liste complète des formats de fichiers pris en charge, reportez-vous à la description de l’utilitaire IC dans la documentation sur la diffusion d’images.

## Propriétés {#section-e68d03788d534e2184147987d51dfd0f}

Attribut de matériau. Obligatoire pour tous les matériaux, à l&#39;exception de la couleur unie (non autorisée pour les matériaux de couleur unie). Toutes les chaînes sont sensibles à la casse. *`index`* doit être égal ou supérieur à 0.

## Par défaut {#section-dde549c1917540dc8f9555962202da3c}

Aucune

## Exemple {#section-675865444f8a4d35b9fc6e58b36e3438}

Un MSS pour une armoire colorée avec une texture répétable distincte :

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

Le même matériau peut être situé dans un catalogue de matières `'cat`&#39; dans l&#39;enregistrement &quot; `12-3-2`&quot; :

`…&obj=cabinets&src=cat/12-3-2&…`

Demande imbriquée envoyée à Image Serving pour obtenir une image de texture :

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Voir aussi {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Catalogues](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2) de matières,  [attribut::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402),  [attribut::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
