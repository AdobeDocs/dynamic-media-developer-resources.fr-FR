---
description: 'Scene7 Image Serving se compose des composants suivants : '
solution: Experience Manager
title: Composants de diffusion d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

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
   <td colname="col1"> <p>Contrôleur de serveur </p> </td> 
   <td colname="col2"> <p>Exécutable autonome responsable du démarrage, de l'arrêt et de la santé des autres composants. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Fournit l’environnement de la plupart des composants basés sur Java. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Service de surveillance/d’alerte </p> </td> 
   <td colname="col2"> <p>Application J2EE. Permet la surveillance du serveur et l’envoi d’alertes par courrier électronique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serveur de plateformes </p> </td> 
   <td colname="col2"> <p>Application J2EE. Gère les connexions client, la journalisation et les communications avec d'autres composants. Accès HTTP à <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Service de mise en cache </p> </td> 
   <td colname="col2"> <p>Application J2EE. Gère les caches de données de Platform Server. Accès HTTP à l’adresse /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>Effectue toutes les opérations d’E/S de traitement d’image et de fichiers image. Les exécutables 32 bits et 64 bits sont disponibles pour Linux (32 bits uniquement pour Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Composant de rendu de texte ATE </p> </td> 
   <td colname="col2"> <p>Une ou plusieurs instances du service de rendu de texte peuvent être principales lorsque des opérations <span class="codeph"> textPs=</span> sont exécutées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Composant de rendu SVG </p> </td> 
   <td colname="col2"> <p>Application Java autonome (non hébergée par Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rendu d’image Dynamic Media (aka. Render Server) </p> </td> 
   <td colname="col2"> <p>Nécessite une licence distincte pour l’activation. Accès HTTP à <span class="filepath"> /ir/render</span>. Toutes les fonctionnalités de rendu d’image sont intégrées au serveur de plateformes et au serveur d’images, sans composants exécutables distincts. </p> </td> 
  </tr> 
 </tbody> 
</table>

D’autres paramètres de configuration sont fournis par le catalogue par défaut ( [!DNL default.ini]) ou des catalogues d’images spécifiques (voir [Catalogues d’images](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) pour plus de détails).
