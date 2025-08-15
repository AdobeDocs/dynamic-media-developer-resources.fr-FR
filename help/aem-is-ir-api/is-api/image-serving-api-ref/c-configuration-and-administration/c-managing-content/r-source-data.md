---
description: Les fichiers de données source de la diffusion d’images comprennent les fichiers d’image et de masque, les polices et les profils ICC.
solution: Experience Manager
title: Données Source
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Données Source{#source-data}

Les fichiers de données source de la diffusion d’images comprennent les fichiers d’image et de masque, les polices et les profils ICC.

Tous les fichiers de données sources doivent être accessibles au serveur d’images. La diffusion d’images offre plusieurs alternatives pour spécifier l’emplacement des fichiers de données :

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
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> chemin d’accès et le nom du fichier image relatif spécifiés dans une requête HTTP de diffusion d’images</span> </p></td> 
 </tr> 
</table>

Le serveur combine les segments de chemin d’accès de droite à gauche jusqu’à ce qu’un chemin d’accès absolu soit établi.

Tous les segments `*`rootPath`*` peuvent être des segments de chemin d’accès vides, relatifs ou absolus.

`*`catalogPath`*` est un chemin/nom de fichier absolu ou relatif. `*`requestPath`*` doit être un chemin/nom de fichier relatif.

`Multiple IS::RootPath` valeurs peuvent être définies dans ImageServerRegistry.xml (ou par le biais de l’interface d’administration). Cela permet de distribuer les fichiers de données sources sur plusieurs systèmes de fichiers. Le serveur d’images tente d’accéder à d’autres chemins dans l’ordre spécifié jusqu’à ce que le fichier de données soit trouvé.

Il est possible d’ajouter de nouveaux fichiers de données de n’importe quel type à tout moment sans arrêter le serveur.
