---
description: 'Scene7 Image Serving se compose des composants suivants : '
seo-description: 'Scene7 Image Serving se compose des composants suivants : '
seo-title: Composants de diffusion d’images
solution: Experience Manager
title: Composants de diffusion d’images
topic: Scene7 Image Serving - Image Rendering API
uuid: 84e04972-32ce-4aca-aae6-d5b8bbe761e6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Composants de diffusion d’images{#image-serving-components}

Scene7 Image Serving se compose des composants suivants :

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Composant </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Superviseur de serveur </p> </td> 
   <td colname="col2"> <p>Exécutable autonome responsable du démarrage, de l'arrêt et de la santé des autres composants. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Fournit le   pour la plupart des composants basés sur Java. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Service de surveillance/d’alerte </p> </td> 
   <td colname="col2"> <p>Application J2EE. Fournit la surveillance du serveur et des alertes par courrier électronique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serveur de plateformes </p> </td> 
   <td colname="col2"> <p>Application J2EE. Gère les connexions client, la journalisation et les communications avec d’autres composants. Accès HTTP à <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Service de mise en cache </p> </td> 
   <td colname="col2"> <p>Application J2EE. Gère les caches de données du serveur de plateformes. Accès HTTP sur /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>Exécute toutes les opérations d’E/S de traitement d’image et de fichiers d’images. Les exécutables 32 bits et 64 bits sont disponibles pour Linux (32 bits uniquement pour Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Composant de rendu de texte ATE </p> </td> 
   <td colname="col2"> <p>Une ou plusieurs instances du service de rendu de texte peuvent être actives lors de l’exécution des opérations <span class="codeph"> textPs=</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Composant de rendu SVG </p> </td> 
   <td colname="col2"> <p>Application Java autonome (non hébergée par Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rendu d’image Scene7 (par ex. Render Server) </p> </td> 
   <td colname="col2"> <p>Nécessite une licence distincte pour l’activation. Accès HTTP à <span class="filepath"> /ir/render</span>. Toutes les fonctionnalités de rendu d’image sont intégrées au serveur de plateformes et au serveur d’images, sans composants exécutables distincts. </p> </td> 
  </tr> 
 </tbody> 
</table>

D’autres paramètres de configuration sont fournis par le catalogue par défaut ( [!DNL default.ini]) ou des catalogues d’images spécifiques (voir Catalogues [d’](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) images pour plus de détails).
