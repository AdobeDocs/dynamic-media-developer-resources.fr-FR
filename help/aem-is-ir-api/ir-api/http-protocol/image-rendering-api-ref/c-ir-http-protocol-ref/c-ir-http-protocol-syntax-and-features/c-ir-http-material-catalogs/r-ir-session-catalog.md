---
title: Catalogue de sessions
description: Le catalogue de sessions est le catalogue de matériaux qui fournit des attributs de session pour la requête, et une valeur catId par défaut pour toutes les commandes src=, vignette= et icc=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Catalogue de sessions{#session-catalog}

Le catalogue de sessions est le catalogue de matières qui fournit des attributs de session pour la requête, ainsi qu’une valeur catId par défaut pour toutes les commandes `src=`, `vignette=` et `icc=`.

Le catalogue de sessions est spécifié comme premier élément de chemin d’accès du chemin d’accès de requête HTTP (suivant immédiatement le nom du serveur). Si le premier élément de chemin ne correspond à aucun attribut::RootId d’un catalogue, le catalogue par défaut est utilisé comme catalogue de sessions.

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
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> Chemin d’accès racine pour les fichiers de données de matériaux </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::VignettePath</span> </p> </td> 
   <td> <p> Chemin racine des fichiers de vignettes </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::IccProfileRgb</span> </p> </td> 
   <td> <p> Espace de travail par défaut si une vignette n’incorpore pas de profil ICC </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootUrl</span> </p> </td> 
   <td> <p> URL racine pour les chemins de fichiers HTTP relatifs dans les commandes <span class="codeph"> src=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::ShowOverlapObjs</span> </p> </td> 
   <td> <p> État d’affichage/de masquage initial pour les objets de chevauchement </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> Valeur de durée de vie de l’image de réponse pour les caches du serveur proxy et du navigateur </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::MaxPix</span> </p> </td> 
   <td> <p> Largeur et hauteur maximales de l’image de réponse autorisée </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
   <td> <p> Valeurs par défaut de <span class="codeph"> wid=</span> et <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Format</span> </p> </td> 
   <td> <p> Valeur par défaut pour <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::JpegQuality</span> </p> </td> 
   <td> <p> Valeur par défaut pour <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::TiffEncoding</span> </p> </td> 
   <td> <p> Type de compression pour la sortie d’image par TIFF </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attribut <span class="codeph"> ::Accentuer</span> </p> </td> 
   <td> <p> Valeur par défaut pour <span class="codeph"> sharpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailSel</span> </p> </td> 
   <td> <p> Spécifie le comportement lorsqu’une commande <span class="codeph"> sel=</span> échoue </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailObj</span> </p> </td> 
   <td> <p> Spécifie le comportement lorsqu’une commande <span class="codeph"> obj=</span> échoue </p> </td> 
  </tr> 
 </tbody> 
</table>
