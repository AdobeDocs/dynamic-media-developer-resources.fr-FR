---
description: Le catalogue de session est le catalogue de matières qui fournit des attributs de session pour la requête, ainsi qu’une valeur catId par défaut pour toutes les commandes src=, vignette= et icc=.
seo-description: Le catalogue de session est le catalogue de matières qui fournit des attributs de session pour la requête, ainsi qu’une valeur catId par défaut pour toutes les commandes src=, vignette= et icc=.
seo-title: Catalogue de sessions
solution: Experience Manager
title: Catalogue de sessions
topic: Scene7 Image Serving - Image Rendering API
uuid: 69c0f6cd-dfaf-47bf-bdd9-7abb4e6f7465
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Catalogue de sessions{#session-catalog}

Le catalogue de session est le catalogue de matières qui fournit des attributs de session pour la requête, ainsi qu’une valeur catId par défaut pour toutes les commandes src=, vignette= et icc=.

Le catalogue de session est spécifié comme premier élément de chemin du chemin d’accès de la requête HTTP (juste après le nom du serveur). Si le premier élément de chemin ne correspond pas à attribute::RootId d’un catalogue, le catalogue par défaut est utilisé comme catalogue de session.

Le catalogue de session fournit les valeurs par défaut suivantes pour la session :

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attribut </p> </th> 
   <th class="entry"> <p>Remarques </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribut:RootPath</span> </p> </td> 
   <td> <p> Chemin d’accès racine pour les fichiers de données matières </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut:VignettePath</span> </p> </td> 
   <td> <p> Chemin racine des fichiers de vignette </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::IccProfileRgb</span> </p> </td> 
   <td> <p> Espace colorimétrique de travail par défaut si une vignette n’incorpore pas de ICC  </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut:RootUrl</span> </p> </td> 
   <td> <p> URL racine pour les chemins de fichier HTTP relatifs dans les commandes <span class="codeph"> src=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut:ShowOverlapObject</span> </p> </td> 
   <td> <p> Etat initial d’affichage/masquage des objets de chevauchement </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut:Expiration</span> </p> </td> 
   <td> <p> Durée de vie de l’image de réponse pour les caches du serveur proxy et du navigateur </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::MaxPix</span> </p> </td> 
   <td> <p> Largeur et hauteur maximales autorisées pour l’image de réponse </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut:DefaultPix</span> </p> </td> 
   <td> <p> Valeurs par défaut pour <span class="codeph"> wid=</span> et <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut:Format</span> </p> </td> 
   <td> <p> Valeur par défaut de <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::JpegQuality</span> </p> </td> 
   <td> <p> Valeur par défaut de <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::TiffEncoding</span> </p> </td> 
   <td> <p> Type de compression pour la sortie d’image TIFF </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::Accentuer</span> </p> </td> 
   <td> <p> Valeur par défaut de <span class="codeph"> sharpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::OnFailSel</span> </p> </td> 
   <td> <p> Indique le comportement en cas d’échec d’une commande <span class="codeph"> sel=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut::OnFailObj</span> </p> </td> 
   <td> <p> Indique le comportement en cas d’échec d’une commande <span class="codeph"> obj=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

