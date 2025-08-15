---
description: Propriétés d’un fichier image.
solution: Experience Manager
title: Infos sur l’image
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 058c74b2-634c-49b9-88ab-ab72a030983c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---

# [!DNL ImageInfo]{#imageinfo}

Propriétés d’un fichier image.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL originalPath]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Chemin d’accès relatif au fichier d’origine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> [!DNL originalFile]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Nom du fichier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> [!DNL optimizedPath]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Chemin d’accès au fichier image optimisé pour IPS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL optimizedFile]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Fichier image optimisé pour IPS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL maskPath]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Chemin du masque de l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL maskFile]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Nom de fichier du masque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL width]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :int</span> </td> 
   <td colname="col3"> <p>Largeur d’image en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL height]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :int</span> </td> 
   <td colname="col3"> <p>Hauteur d’image en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL fileSize]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :int</span> </td> 
   <td colname="col3"> <p>Taille de l’image en octets. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL resolution]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :double</span> </td> 
   <td colname="col3"> <p>Pixels par pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL sku]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>ID de produit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL description]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Description de l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL comments]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Commentaires (obsolète). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL userData]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Informations utilisateur associées à l’image (obsolète). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL anchorX]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :int</span> </td> 
   <td colname="col3"> <p>Point d’ancrage horizontal en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL anchorY]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :int</span> </td> 
   <td colname="col3"> <p>Point d’ancrage vertical en piexels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL urlModifier]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Paramètre d’URL du serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL urlPostApplyModifier]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Paramètres concaténés à la fin d’urlModifier<span class="codeph"></span>. Format de chaîne de requête Liste des paramètres qui sont des commandes adressées au serveur d’images. Les valeurs se trouvent dans le guide du protocole Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL zoomTargets]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ZoomTargetArray</span> </td> 
   <td colname="col3"> <p>Tableau de cibles de zoom (5 max). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL masks]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :MaskArray</span> </td> 
   <td colname="col3"> <p>Tableau de masques. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL imageMaps]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ImageMapsArray</span> </td> 
   <td colname="col3"> <p>Tableau de zones cliquables. </p> </td> 
  </tr> 
 </tbody> 
</table>
