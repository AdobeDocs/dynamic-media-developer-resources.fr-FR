---
description: Tous les fichiers de configuration se trouvent dans install_folder/conf et sont modifiables avec la plupart des éditeurs de texte. Il se peut que le serveur doive être redémarré pour que les modifications prennent effet.
solution: Experience Manager
title: Fichiers de configuration du serveur
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Fichiers de configuration du serveur{#server-configuration-files}

Tous les fichiers de configuration se trouvent dans install_folder/conf et sont modifiables avec la plupart des éditeurs de texte. Il se peut que le serveur doive être redémarré pour que les modifications prennent effet.

>[!NOTE]
>
>La plupart des fichiers de configuration de serveur contiennent des propriétés et des valeurs supplémentaires qui ne sont pas décrites dans ce document. Ces propriétés sont destinées à un usage interne du serveur et ne doivent pas être modifiées, sauf si le support technique de Dynamic Media l&#39;exige expressément.

Ce document traite des paramètres des fichiers de configuration suivants :

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Fichier de configuration</b> </th> 
   <th class="entry"> <b>Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisorRegistry.xml</span> </p> </td> 
   <td> <p>Configuration du contrôleur de serveur. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Configuration de Tomcat. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>Configuration du serveur de plateformes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>Configuration du service de catalogue. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf</span> </p> </td> 
   <td> <p>Configuration de la surveillance du serveur. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>Configuration du serveur d’images. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les fichiers de configuration sont décrits plus en détail plus loin dans ce document.
