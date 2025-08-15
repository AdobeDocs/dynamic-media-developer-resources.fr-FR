---
title: SRC
description: Fichier matériel. Spécifie les données de matière, soit sous la forme d’une référence unique de catalogue de matériaux, soit sous la forme d’une ou deux images ou fichiers de données de matériau, séparés par une virgule.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 1%

---

# SRC{#src}

Fichier matériel. Spécifie les données de matériau, soit sous la forme d&#39;une référence unique de catalogue de matériaux, soit sous la forme d&#39;un ou de deux fichiers d&#39;image ou de données de matériaux, séparés par une virgule.

`src = *`entrée`*|{{ *`de catalogue Fichier de matériau`*| *`intégré`*}[, *` `*]`

`srcE= *`nom`*`

`srcN= *`index`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> entrée de catalogue</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/]<span class="varname"> [ catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> beddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&lbrace;'is&lbrace;'<span class="varname"> isReq</span>'&rbrace;'&rbrace;|&lbrace;'ir&lbrace;'<span class="varname"> irReq</span>'&rbrace;'|&lbrace;'&lbrace;'<span class="varname"> foreignReq</span>'&rbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>ID catalogue de matières (attribut <span class="codeph"> : RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Entrée du catalogue de matières (<span class="codeph"> catalog::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>Fichier de style de matériau (<span class="filepath"> .vnc</span> ou <span class="filepath"> .vnw</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>Fichier de données d’image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>Demande au serveur d’images. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>Demande au rendu d’images. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>Demande à un serveur étranger. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nom</span> </p></td> 
  <td class="stentry"> <p>Nom d’un matériau incorporé. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> index</span> </p></td> 
  <td class="stentry"> <p>Numéro d’index basé sur 0 pour un matériau incorporé. </p></td> 
 </tr> 
</table>

Les matériaux Texture répétable, Décalcomanie et Papier peint nécessitent une seule image, qui peut être spécifiée sous la forme d’un fichier ou d’une requête incorporée.

Les matériaux d&#39;armoire nécessitent un fichier de style d&#39;armoire ( [!DNL .vnc]), qui ne peut pas être spécifié comme une requête imbriquée. Un fichier image de texture est facultatif pour les armoires et, si spécifié, il peut s&#39;agir d&#39;un fichier ou d&#39;une requête incorporée.

Les matériaux de revêtement de fenêtre nécessitent un fichier de style de revêtement de fenêtre ([!DNL .vnw]), qui ne peut pas être spécifié comme une demande imbriquée. Un fichier de texture est facultatif et, si spécifié, il peut s&#39;agir d&#39;un fichier ou d&#39;une requête incorporée.

Le rendu d’image utilise les mêmes règles que le service d’images pour la recherche de catalogues de matériaux, d’entrées de catalogue et de fichiers de données. Reportez-vous à la description du type de données *`object`* dans la documentation du service d’images pour plus d’informations.

*`materialFile`* est un chemin d’accès relatif à `attribute::RootPath`.

*`foreignReq`* Peut être une URL relative à `attribute::RootUrl` ou une URL absolue si `attribute::AllowDirectUrls` est défini.

Si *`catId`* n’est pas spécifié, le catalogue de sessions est utilisé.

`srcE=` et `srcN=` donnent accès aux matériaux intégrés dans la vignette.

## Formats de fichiers pris en charge {#section-f2186d3eef834fc8bbecb2bc68daacad}

Le rendu d’image prend en charge les mêmes formats d’image source que la diffusion d’images Dynamic Media.

Les applications qui nécessitent des données image dans plusieurs résolutions différentes fonctionnent mieux lors de l’utilisation du format multi-résolution Scene7 pyramid TIFF (PTIFF). Image Serving inclut l’utilitaire Image Converter (IC) qui crée des images PTIFF à partir de n’importe quel format pris en charge.

Reportez-vous à la description de l’utilitaire IC dans la documentation Image Serving pour obtenir la liste complète des formats de fichiers pris en charge.

## Propriétés {#section-e68d03788d534e2184147987d51dfd0f}

Attribut Material. Requis pour tous les matériaux sauf la couleur unie (non autorisée pour les matériaux de couleur unie). Toutes les chaînes respectent la casse. *`index`* Doit être égale ou supérieure à 0.

## Par défaut {#section-dde549c1917540dc8f9555962202da3c}

Aucune

## Exemple {#section-675865444f8a4d35b9fc6e58b36e3438}

MSS pour une armoire colorée avec une texture répétable distincte :

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

Le même matériau peut se trouver dans un catalogue de matériaux `'cat`&#39; dans l&#39;enregistrement &#39; `12-3-2`&#39; :

`…&obj=cabinets&src=cat/12-3-2&…`

Requête imbriquée au service d’images pour obtenir une image de texture :

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Voir aussi {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Catalogues de matériaux](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402), [attribute::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
