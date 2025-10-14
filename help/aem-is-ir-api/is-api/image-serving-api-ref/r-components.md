---
title: Composants de diffusion d’images
description: Le service d’images Dynamic Media se compose des composants suivants.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---

# Composants de diffusion d’images{#image-serving-components}

La diffusion d’images Dynamic Media se compose des composants suivants :

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
   <td colname="col2"> <p>Un exécutable autonome chargé de démarrer, d’arrêter et d’assurer l’intégrité des autres composants. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Il fournit l’environnement pour la plupart des composants basés sur Java. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Service de surveillance/d’alerte </p> </td> 
   <td colname="col2"> <p>Application J2EE. Surveillance du serveur et alertes par e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>Application J2EE. Gère les connexions client, la journalisation et les communications avec d’autres composants. Accès HTTP à <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Service de mise en cache </p> </td> 
   <td colname="col2"> <p>Application J2EE. Gère les caches de données du [!DNL Platform Server]. Accès HTTP à /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>Il effectue toutes les opérations de traitement des images et d’E/S de fichiers images. Les exécutables 32 bits et 64 bits sont disponibles pour Linux® (32 bits uniquement pour Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Composant de rendu de texte DATE </p> </td> 
   <td colname="col2"> <p>Une ou plusieurs instances du service de rendu de texte peuvent être actives lors de l'exécution d'opérations textPs=<span class="codeph"> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Composant de rendu SVG </p> </td> 
   <td colname="col2"> <p>Application Java™ autonome (non hébergée par Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rendu d’image Dynamic Media (alias. Serveur de rendu) </p> </td> 
   <td colname="col2"> <p>L’activation nécessite une licence distincte. Accès HTTP à <span class="filepath"> /ir/render</span>. Toutes les fonctionnalités de rendu d’image sont intégrées dans le [!DNL Platform Server] et le serveur d’images, sans composants exécutables distincts. </p> </td> 
  </tr> 
 </tbody> 
</table>

Des paramètres de configuration supplémentaires sont fournis par le catalogue par défaut ( [!DNL default.ini]) ou des catalogues d’images spécifiques (voir [&#x200B; Catalogues d’images](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) pour plus d’informations).
