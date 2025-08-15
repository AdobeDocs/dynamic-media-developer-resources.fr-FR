---
title: Fichiers de configuration du serveur
description: Tous les fichiers de configuration se trouvent dans le dossier install_folder/conf et sont modifiables avec la plupart des éditeurs de texte. Redémarrez le serveur pour que les modifications soient prises en compte.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Fichiers de configuration du serveur{#server-configuration-files}

Tous les fichiers de configuration se trouvent dans le `install_folder/conf` et sont modifiables avec la plupart des éditeurs de texte. Redémarrez le serveur pour que les modifications soient prises en compte.

>[!NOTE]
>
>La plupart des fichiers de configuration du serveur contiennent des propriétés et des valeurs supplémentaires qui ne sont pas décrites dans ce document. Ces propriétés sont destinées à une utilisation interne du serveur et ne doivent pas être modifiées, sauf instructions contraires du support technique de Dynamic Media.

Ce document présente les paramètres des fichiers de configuration suivants :

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Fichier de configuration </b> </th> 
   <th class="entry"> <b> Description </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisorRegistry.xml</span> </p> </td> 
   <td> <p>Configuration du Superviseur de serveur. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Configuration de Tomcat. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>[!DNL Platform Server] configuration. </p> </td> 
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

Les fichiers de configuration sont traités plus en détail plus loin dans ce document.
