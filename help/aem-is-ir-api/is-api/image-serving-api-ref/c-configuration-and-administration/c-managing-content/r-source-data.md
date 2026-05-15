---
description: Les fichiers de données source de la diffusion d’images comprennent les fichiers d’image et de masque, les polices et les profils ICC.
solution: Experience Manager
title: Données Source
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
TQID: 'https://experienceleague.adobe.com/36EvEOjHZ8ik-gps-vaap5PhFCf5rwV9ecfkKHZcIhk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
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
