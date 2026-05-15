---
description: Script de contrôle de la diffusion d’images. Ce script permet de démarrer, d’arrêter ou de redémarrer le superviseur du serveur de diffusion d’images, qui à son tour démarre, arrête ou redémarre tous les autres composants de la diffusion d’images.
solution: Experience Manager
title: Diffusion d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
TQID: 'https://experienceleague.adobe.com/KyiS-GblbCE-Q4Exrdz8T1W5thFn9cHellB-1-QYZaw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
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
   <td colname="col1"> <p> </span> de début de <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Démarrez le Superviseur de serveur et tous les autres composants de diffusion d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop </span> </p> </td> 
   <td colname="col2"> <p> Arrêtez tous les composants de diffusion d’images, y compris le superviseur de serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de redémarrage <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Redémarrez tous les composants de diffusion d’images, y compris le superviseur de serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> redémarrage { ps | is | svg } </span> </p> </td> 
   <td colname="col2"> <p> Redémarre Tomcat/[!DNL Platform Server], le serveur d’images ou SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> statut [ ps | is | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Renvoie les informations de disponibilité et d’utilisation actuelle de la mémoire pour le serveur d’images, Tomcat/[!DNL Platform Server] et SVGserver, ou l’état du serveur spécifié uniquement ; un message d’information est renvoyé à la place si le superviseur du serveur n’est pas en cours d’exécution. </p> </td> 
  </tr> 
 </tbody> 
</table>
