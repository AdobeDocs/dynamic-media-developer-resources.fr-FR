---
description: Script de contrôle Image Serving. Ce script est utilisé pour début, arrêter ou redémarrer le superviseur du serveur Image Serving qui, à son tour, début, arrête ou redémarre tous les autres composants Image Serving.
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 2%

---


# ImageServing{#imageserving}

Script de contrôle Image Serving. Ce script est utilisé pour début, arrêter ou redémarrer le superviseur du serveur Image Serving qui, à son tour, début, arrête ou redémarre tous les autres composants Image Serving.

## Utilisation {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`command`*`

## Commandes {#section-90436a0b0f70435f9ac42dafeed2c17b}

<table id="table_692C6A043F9747C88929FF20373EC88C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Commande </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> commencer </span> </p> </td> 
   <td colname="col2"> <p> Début du contrôleur de serveur et de tous les autres composants de diffusion d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop  </span> </p> </td> 
   <td colname="col2"> <p> Arrêtez tous les composants de diffusion d’images, y compris le contrôleur de serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Redémarrer </span> </p> </td> 
   <td colname="col2"> <p>Redémarrez tous les composants de diffusion d’images, y compris le contrôleur de serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> redémarrer { ps | is | svg }  </span> </p> </td> 
   <td colname="col2"> <p> Redémarre Tomcat/Platform Server, Image Server ou SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps | is | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>Renvoie les informations d’utilisation de la mémoire et du temps de disponibilité pour Image Server, Tomcat/Platform Server et SVGserver, ou l’état pour le serveur spécifié uniquement ; un message d’information est renvoyé si le contrôleur de serveur n’est pas en cours d’exécution. </p> </td> 
  </tr> 
 </tbody> 
</table>

