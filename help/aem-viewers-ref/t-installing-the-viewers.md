---
title: Installation de plusieurs visionneuses Dynamic Media sur le même serveur
description: Instructions d’installation de l’API Dynamic Media Viewers.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Installation de plusieurs visionneuses sur le même serveur{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instructions pour l’installation de l’API des visionneuses Dynamic Media.

Installez et testez Image Serving avant d’installer les visionneuses Image Server.

Copiez les fichiers IS Viewers sur votre disque dur, puis déployez-les `s7viewers.war` dans le `../ImageServing/webapps` répertoire. Consultez votre documentation Image Serving pour obtenir des instructions sur le déploiement, le démarrage, l’arrêt et la gestion d’Image Server.

>[!NOTE]
>
>Il n’y a pas d’installation de mise à niveau pour les visionneuses Image Server. Adobe vous recommande de sauvegarder tout répertoire Dynamic Media visionneuses (s7viewers) existant avant de poursuivre l’installation.

**Pour installer plusieurs visionneuses sur le même serveur :**

1. Renommez la visionneuse .war au contexte souhaité et déployez le fichier à l’emplacement souhaité.
1. Définissez le `this.isViewerRoot` paramètre dans `config.js`.
1. Ouvrez `config.js` à la racine du dossier de visionneuse nouvellement créé.
1. Définissez le paramètre `this.isViewerRoot = "/s7viewers"` sur le contexte du `s7viewers.war` fichier. Par exemple, `"/s7viewers-4.0"`.
1. Enregistrez le fichier et fermez-le.
