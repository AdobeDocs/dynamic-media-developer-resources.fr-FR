---
description: Le catalogue de sessions est le catalogue de matières qui fournit des attributs de session pour la requête, ainsi qu’une valeur catId par défaut pour toutes les commandes src=, vignette= et icc=.
seo-description: Le catalogue de sessions est le catalogue de matières qui fournit des attributs de session pour la requête, ainsi qu’une valeur catId par défaut pour toutes les commandes src=, vignette= et icc=.
seo-title: Catalogue de sessions
solution: Experience Manager
title: Catalogue de sessions
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 69c0f6cd-dfaf-47bf-bdd9-7abb4e6f7465
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---


# Catalogue de session{#session-catalog}

Le catalogue de sessions est le catalogue de matières qui fournit des attributs de session pour la requête, ainsi qu’une valeur catId par défaut pour toutes les commandes src=, vignette= et icc=.

Le catalogue de sessions est spécifié comme premier élément de chemin d’accès du chemin d’accès de la requête HTTP (juste après le nom du serveur). Si le premier élément de chemin ne correspond pas à attribute::RootId d’un catalogue, le catalogue par défaut est utilisé en tant que catalogue de session.

Le catalogue de sessions fournit les valeurs par défaut de session suivantes :

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attribut </p> </th> 
   <th class="entry"> <p>Remarques </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::RootPath</span> </p> </td> 
   <td> <p> Chemin d’accès racine pour les fichiers de données matières </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::VignettePath</span> </p> </td> 
   <td> <p> Chemin d’accès racine pour les fichiers de vignettes </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::IccProfileRgb</span> </p> </td> 
   <td> <p> Espace colorimétrique de travail par défaut si une vignette n’incorpore pas de profil ICC </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::RootUrl</span> </p> </td> 
   <td> <p> URL racine pour les chemins de fichier HTTP relatifs dans les commandes <span class="codeph"> src=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::ShowOverlapObjects</span> </p> </td> 
   <td> <p> Etat initial d’affichage/de masquage des objets de chevauchement </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::Expiration</span> </p> </td> 
   <td> <p> Valeur de durée de vie de l’image de réponse pour les caches du serveur proxy et du navigateur </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::MaxPix</span> </p> </td> 
   <td> <p> Largeur et hauteur maximales de l’image de réponse autorisée </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::DefaultPix</span> </p> </td> 
   <td> <p> Valeurs par défaut pour <span class="codeph"> wid=</span> et <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::Format</span> </p> </td> 
   <td> <p> Valeur par défaut de <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::JpegQuality</span> </p> </td> 
   <td> <p> Valeur par défaut de <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::TiffEncoding</span> </p> </td> 
   <td> <p> Type de compression pour la sortie d’image TIFF </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::Accentuer</span> </p> </td> 
   <td> <p> Valeur par défaut de <span class="codeph"> sharpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::OnFailSel</span> </p> </td> 
   <td> <p> Indique le comportement lorsqu’une commande <span class="codeph"> sel=</span> échoue. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::OnFailObj</span> </p> </td> 
   <td> <p> Indique le comportement lorsqu’une commande <span class="codeph"> obj=</span> échoue. </p> </td> 
  </tr> 
 </tbody> 
</table>

