---
description: Instructions d’installation de l’API Dynamic Media Viewers.
seo-description: Instructions d’installation de l’API Dynamic Media Viewers.
seo-title: Installation de plusieurs visionneuses sur le même serveur
solution: Experience Manager
title: Installation de plusieurs visionneuses sur le même serveur
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: a0983053795cc119eb57386c005e1f8a7c2fa3e4
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# Installation de plusieurs visionneuses sur le même serveur{#installing-multiple-viewers-on-the-same-server}

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instructions d’installation de l’API des visionneuses Dynamic Media.

Installez et testez Image Serving avant d’installer les visionneuses Image Serving.

Copiez les fichiers des visionneuses IS sur votre disque dur, puis déployez le fichier `s7viewers.war` dans le répertoire `../ImageServing/webapps`. Pour obtenir des instructions sur la manière de déployer, de début, d’arrêter et de gérer le serveur Image Server, reportez-vous à la documentation relative à Image Serving.

>[!NOTE]
>
>Aucune mise à niveau n’est installée pour les visionneuses Image Serving. Adobe vous recommande de sauvegarder tout répertoire de lecteurs de contenu Dynamic Media existant avant de poursuivre l’installation.

**Pour installer les visionneuses sur le même serveur**

1. Renommez le fichier .war dans le contexte souhaité et déployez-le à l’emplacement souhaité.
1. Définissez le paramètre `this.isViewerRoot` dans `config.js`.
1. Ouvrez `config.js` situé dans la racine du dossier de lecteur de contenu que vous venez de créer.
1. Définissez le paramètre `this.isViewerRoot = "/s7viewers"` sur le contexte du fichier `s7viewers.war`. Par exemple, `"/s7viewers-4.0"`. Enregistrez et fermez le fichier.
1. Enregistrez le fichier et fermez-le.
