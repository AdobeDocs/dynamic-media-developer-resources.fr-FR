---
title: src
description: Fichier de matière. Spécifie les données de matériau, sous la forme d’une référence de catalogue de matériaux unique, ou sous la forme d’une ou deux images ou de fichiers de données de matériau, séparés par une virgule.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 1%

---

# src{#src}

Fichier de matière. Spécifie les données de matériau, sous la forme d’une référence de catalogue de matériaux unique, ou sous la forme d’une ou deux images ou de fichiers de données de matériau, séparés par une virgule.

`src = *`catalogEntry`*|{{ *`matérielFile`*| *`embeddedReq`*}[, *`matérielFile`*]`

`srcE= *`name`*`

`srcN= *`index`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> matterFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;location;'is&amp;location;'<span class="varname"> isReq</span>'&amp;accolade;'&amp;accolade;|&amp;location;'ir&amp;location;'<span class="varname"> irReq</span>'&amp;accolade;'|&amp;accolade;'<span class="varname"> ForeignReq</span>'&amp;accolade;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>Identifiant du catalogue de matières (<span class="codeph"> attribute::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Entrée de catalogue de matières (<span class="codeph"> catalog::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>Fichier de style de matière (<span class="filepath"> .vnc</span> ou <span class="filepath"> .vnw</span>). </p></td> 
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
  <td class="stentry"> <p><span class="varname"> ForeignReq</span> </p></td> 
  <td class="stentry"> <p>Demande à un serveur étranger. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p></td> 
  <td class="stentry"> <p>Nom d’un matériau incorporé. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> index</span> </p></td> 
  <td class="stentry"> <p>Numéro d’index de base 0 pour un matériau incorporé. </p></td> 
 </tr> 
</table>

Les matériaux de texte, de décal et de papier peint répétables requièrent une seule image, qui peut être spécifiée sous la forme d’un fichier ou d’une requête incorporée.

Les documents du Cabinet requièrent un fichier de style Cabinet ( [!DNL .vnc]), qui ne peut pas être spécifié en tant que requête imbriquée. Un fichier image de texture est facultatif pour les armoires et, s’il est spécifié, il peut s’agir d’un fichier ou d’une requête incorporée.

Les matériaux de recouvrement de fenêtre nécessitent un fichier de style de recouvrement de fenêtre ( [!DNL .vnw]), qui ne peut pas être spécifié en tant que requête imbriquée. Un fichier de texture est facultatif et, s’il est spécifié, il peut s’agir d’un fichier ou d’une requête incorporée.

Le rendu d’image utilise les mêmes règles que le service d’images pour rechercher des catalogues de matériaux, des entrées de catalogue et des fichiers de données. Pour plus d’informations, reportez-vous à la description du type de données *`object`* dans la documentation du serveur d’images.

*`materialFile`* Est un chemin relatif à `attribute::RootPath`.

*`foreignReq`* Peut être une URL relative à `attribute::RootUrl` ou une URL absolue si `attribute::AllowDirectUrls` est défini.

Si *`catId`* n’est pas spécifié, le catalogue de sessions est utilisé.

`srcE=` et `srcN=` donnent accès aux matériaux incorporés dans la vignette.

## Formats de fichiers pris en charge {#section-f2186d3eef834fc8bbecb2bc68daacad}

Le rendu d’image prend en charge les mêmes formats d’image source que le service d’images Dynamic Media.

Les applications qui nécessitent des données d’image à plusieurs résolutions différentes fonctionnent mieux avec le format PTIFF (Scene7 pyramid TIFF) à plusieurs résolutions. La diffusion d’images comprend l’utilitaire Image Converter (IC) qui crée des images PTIFF à partir de n’importe quel format pris en charge.

Pour obtenir la liste complète des formats de fichiers pris en charge, reportez-vous à la description de l’utilitaire IC dans la documentation du serveur d’images .

## Propriétés {#section-e68d03788d534e2184147987d51dfd0f}

Attribut de matière. Requis pour tous les matériaux, à l&#39;exception des couleurs solides (non autorisées pour les matériaux de couleur solides). Toutes les chaînes respectent la casse. *`index`* Doit être égal ou supérieur à 0.

## Par défaut {#section-dde549c1917540dc8f9555962202da3c}

Aucune

## Exemple {#section-675865444f8a4d35b9fc6e58b36e3438}

Un MSS pour une armoire colorée avec une texture répétable distincte :

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

Le même matériau peut se trouver dans un catalogue de matériaux `'cat`&#39; dans l&#39;enregistrement &#39; `12-3-2`&#39; :

`…&obj=cabinets&src=cat/12-3-2&…`

Demande imbriquée au serveur d’images pour obtenir une image de texture :

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Voir aussi {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Catalogues de matériaux](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402), [attribute::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
