---
description: Les fichiers de données source de la diffusion d’images comprennent les fichiers d’image et de masque, les polices et les profils ICC.
solution: Experience Manager
title: Données source
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# Données source{#source-data}

Les fichiers de données source de la diffusion d’images comprennent les fichiers d’image et de masque, les polices et les profils ICC.

Tous les fichiers de données source doivent être accessibles au serveur Image Server. La diffusion d’images offre plusieurs alternatives pour spécifier l’emplacement des fichiers de données :

`*`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath  </span></span> </p></td> 
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

Le serveur combine les segments de chemin d’accès de droite à gauche jusqu’à ce qu’un chemin d’accès absolu au fichier soit établi.

Tous les segments `*`rootPath`*` peuvent être vides, relatifs ou absolus.

`*``*` catalogPath est un chemin/nom de fichier absolu ou relatif. `*``*` requestPathdoit être un chemin/nom de fichier relatif.

`Multiple IS::RootPath` peuvent être définies dans ImageServerRegistry.xml (ou par l’interface d’administration). Cela permet de distribuer les fichiers de données source sur plusieurs systèmes de fichiers. Le serveur d’images tentera d’autres chemins d’accès dans l’ordre spécifié jusqu’à ce que le fichier de données soit trouvé.

De nouveaux fichiers de données de toute sorte peuvent être ajoutés à tout moment sans arrêter le serveur.
