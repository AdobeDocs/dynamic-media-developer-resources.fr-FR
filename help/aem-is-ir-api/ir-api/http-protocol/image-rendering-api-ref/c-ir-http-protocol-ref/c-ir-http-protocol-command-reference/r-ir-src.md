---
title: src
description: Fichier des matériaux. Spécifie les données de matériau, soit sous la forme d'une référence unique de catalogue de matériaux, soit sous la forme d'un ou de deux fichiers d'image ou de données de matériaux, séparés par une virgule.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
TQID: 'https://experienceleague.adobe.com/-PushPHP2ZvNu2IFmB-1akxSvlXtDvxStXgFTAw1t-w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 444
ht-degree: 1%

---

# src{#src}

Fichier des matériaux. Spécifie les données de matériau, soit sous la forme d&#39;une référence unique de catalogue de matériaux, soit sous la forme d&#39;un ou de deux fichiers d&#39;image ou de données de matériaux, séparés par une virgule.

`src = *`catalogEntry`*|{{ *`materialFile`*| *`beddedReq`*}[, *`materialFile`*]`

`srcE= *`name`*`

`srcN= *`index`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> beddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'ir&amp;lbrace;'<span class="varname"> irReq</span>'&amp;rbrace;'|&amp;lbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;rbrace;'</span> </p></td> 
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
  <td class="stentry"> <p>Fichier de données image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>Requête au service d’images. </p></td> 
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
  <td class="stentry"> <p><span class="varname"> nom </span> </p></td> 
  <td class="stentry"> <p>Nom d'un matériau incorporé. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> index </span> </p></td> 
  <td class="stentry"> <p>Numéro d'index basé sur 0 pour un matériau incorporé. </p></td> 
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

Les applications qui nécessitent des données d’image dans plusieurs résolutions différentes sont plus performantes lors de l’utilisation du format multi-résolution Scene7 pyramid TIFF (PTIFF). La diffusion d’images inclut l’utilitaire Convertisseur d’images (IC) qui crée des images PTIFF à partir de n’importe quel format pris en charge.

Reportez-vous à la description de l’utilitaire IC dans la documentation du service d’images pour obtenir une liste complète des formats de fichiers pris en charge.

## Propriétés {#section-e68d03788d534e2184147987d51dfd0f}

Attribut Material. Requis pour tous les matériaux sauf la couleur unie (non autorisée pour les matériaux de couleur unie). Toutes les chaînes respectent la casse. *`index`* Doit être supérieur ou égal à 0.

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
