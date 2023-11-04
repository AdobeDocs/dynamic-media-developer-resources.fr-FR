---
description: Les fichiers de données source Image Serving comprennent les fichiers image et de masque, les polices et les profils ICC.
solution: Experience Manager
title: Données source
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Données source{#source-data}

Les fichiers de données source Image Serving comprennent les fichiers image et de masque, les polices et les profils ICC.

Tous les fichiers de données source doivent être accessibles au serveur d’images. La diffusion d’images offre plusieurs alternatives pour spécifier l’emplacement des fichiers de données :

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

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
  <td class="stentry"> <p><span class="codeph"> chemin d’accès relatif au fichier image et nom spécifiés dans une requête HTTP de serveur d’images</span> </p></td> 
 </tr> 
</table>

Le serveur combine les segments de chemin d’accès de droite à gauche jusqu’à ce qu’un chemin d’accès absolu au fichier soit établi.

Tous `*`rootPath`*` les segments peuvent être vides, relatifs ou absolus.

`*`catalogPath`*` est un chemin/nom de fichier absolu ou relatif. `*`requestPath`*` doit être un chemin/nom de fichier relatif.

`Multiple IS::RootPath` Les valeurs peuvent être définies dans ImageServerRegistry.xml (ou par le biais de l’interface d’administration). Cela permet de répartir les fichiers de données sources sur plusieurs systèmes de fichiers. Le serveur d’images tente d’autres chemins d’accès dans l’ordre spécifié jusqu’à ce que le fichier de données soit trouvé.

De nouveaux fichiers de données de tout type peuvent être ajoutés à tout moment sans arrêter le serveur.
