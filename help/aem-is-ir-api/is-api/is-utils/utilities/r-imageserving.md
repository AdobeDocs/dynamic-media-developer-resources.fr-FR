---
description: Script de contrôle de la diffusion d’images. Ce script permet de démarrer, d’arrêter ou de redémarrer le superviseur du serveur de diffusion d’images, qui à son tour démarre, arrête ou redémarre tous les autres composants de la diffusion d’images.
solution: Experience Manager
title: Diffusion d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 1%

---

# Diffusion d’images{#imageserving}

Script de contrôle de la diffusion d’images. Ce script permet de démarrer, d’arrêter ou de redémarrer le superviseur du serveur de diffusion d’images, qui à son tour démarre, arrête ou redémarre tous les autres composants de la diffusion d’images.

## Utilisation {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`commande`*`

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
   <td colname="col1"> <p> <span class="codeph"> de début de </span> </p> </td> 
   <td colname="col2"> <p> Démarrez le Superviseur de serveur et tous les autres composants de diffusion d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop </span> </p> </td> 
   <td colname="col2"> <p> Arrêtez tous les composants de diffusion d’images, y compris le superviseur de serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de redémarrage </span> </p> </td> 
   <td colname="col2"> <p>Redémarrez tous les composants de diffusion d’images, y compris le superviseur de serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> redémarrage { ps | est | svg } </span> </p> </td> 
   <td colname="col2"> <p> Redémarre Tomcat/[!DNL Platform Server], le serveur d’images ou SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Statut de <span class="codeph"> [ ps | est | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Renvoie les informations de disponibilité et d’utilisation actuelle de la mémoire pour le serveur d’images, Tomcat/[!DNL Platform Server] et SVGserver, ou l’état du serveur spécifié uniquement ; un message d’information est renvoyé à la place si le superviseur du serveur n’est pas en cours d’exécution. </p> </td> 
  </tr> 
 </tbody> 
</table>
