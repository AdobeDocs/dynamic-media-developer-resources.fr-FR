---
title: Composants de diffusion d’images
description: La diffusion d’images Dynamic Media se compose des composants suivants.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 2%

---

# Composants de diffusion d’images{#image-serving-components}

Dynamic Media Image Serving se compose des composants suivants :

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
   <td colname="col2"> <p>Exécutable autonome chargé de démarrer, d’arrêter et d’assurer l’intégrité des autres composants. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Il fournit l’environnement pour la plupart des composants Java. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Service de surveillance/d’alerte </p> </td> 
   <td colname="col2"> <p>Application J2EE. Permet la surveillance du serveur et les alertes par e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>Application J2EE. Gère les connexions client, la journalisation et les communications avec d’autres composants. Accès HTTP à <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Service de mise en cache </p> </td> 
   <td colname="col2"> <p>Application J2EE. Gère la variable [!DNL Platform Server]des caches de données de . Accès HTTP à /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>Il effectue toutes les opérations d’E/S de traitement d’image et de fichier image. Les exécutables 32 bits et 64 bits sont disponibles pour Linux® (32 bits uniquement pour Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Composant de rendu de texte ATE </p> </td> 
   <td colname="col2"> <p>Une ou plusieurs instances du service de rendu de texte peuvent être actives lorsque <span class="codeph"> textPs=</span> Les opérations sont exécutées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Composant de rendu SVG </p> </td> 
   <td colname="col2"> <p>Application Java™ autonome (non hébergée par Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rendu d’image Dynamic Media (alias Render Server) </p> </td> 
   <td colname="col2"> <p>Elle nécessite une licence distincte pour être activée. Accès HTTP à <span class="filepath"> /ir/render</span>. Toutes les fonctionnalités de rendu d’image sont intégrées à la fonction [!DNL Platform Server] et le serveur d’images, sans composants exécutables distincts. </p> </td> 
  </tr> 
 </tbody> 
</table>

D’autres paramètres de configuration sont fournis par le catalogue par défaut ( [!DNL default.ini]) ou des catalogues d’images spécifiques (voir [Catalogues d’images](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) pour plus de détails).
