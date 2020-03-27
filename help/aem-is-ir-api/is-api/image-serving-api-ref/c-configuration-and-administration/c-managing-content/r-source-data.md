---
description: Les fichiers de données source du serveur d’images comprennent les fichiers d’image et de masque, les polices et les  ICC.
seo-description: Les fichiers de données source du serveur d’images comprennent les fichiers d’image et de masque, les polices et les  ICC.
seo-title: Données source
solution: Experience Manager
title: Données source
topic: Scene7 Image Serving - Image Rendering API
uuid: d654eee7-ef2d-4546-93bb-72f80c38e018
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Données source{#source-data}

Les fichiers de données source du serveur d’images comprennent les fichiers d’image et de masque, les polices et les  ICC.

Tous les fichiers de données source doivent être accessibles au serveur Image Server. Le serveur d’images propose plusieurs alternatives pour spécifier l’emplacement des fichiers de données :

` *`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogue ::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> chemin d’accès relatif au fichier image et nom spécifiés dans une requête HTTP de diffusion d’images</span> </p></td> 
 </tr> 
</table>

Le serveur combine les segments de chemin de droite à gauche jusqu’à ce qu’un chemin de fichier absolu soit établi.

Tous les segments ` *`rootPath`*` peuvent être des segments de chemin vides, relatifs ou absolus.

` *`catalogPath`*` est un chemin/nom de fichier absolu ou relatif. ` *`requestPath`*` doit être un chemin/nom de fichier relatif.

`Multiple IS::RootPath` peuvent être définies dans ImageServerRegistry.xml (ou par l’intermédiaire de l’interface d’administration). Cela permet de répartir les fichiers de données source sur plusieurs systèmes de fichiers. Le serveur d’images tentera d’autres chemins dans l’ordre spécifié jusqu’à ce que le fichier de données soit trouvé.

De nouveaux fichiers de données de tout type peuvent être ajoutés à tout moment sans arrêter le serveur.
