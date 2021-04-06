---
title: Installation de plusieurs visionneuses Dynamic Media sur le même serveur
description: Instructions d’installation de l’API Dynamic Media Viewers.
solution: Experience Manager
feature: Dynamic Media Classic, Visionneuses, SDK/API
role: Développeur, Professionnel
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
translation-type: tm+mt
source-git-commit: 8207cba7e75c6bff878ef7f11f74b19bb88f1d61
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---

# Installation de plusieurs visionneuses sur le même serveur{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instructions d’installation de l’API des visionneuses Dynamic Media.

Installez et testez Image Serving avant d’installer les visionneuses Image Serving.

Copiez les fichiers des visionneuses IS sur votre disque dur, puis déployez le fichier `s7viewers.war` dans le répertoire `../ImageServing/webapps`. Pour obtenir des instructions sur la manière de déployer, de début, d’arrêter et de gérer le serveur Image Server, reportez-vous à la documentation relative à Image Serving.

>[!NOTE]
>
>Aucune mise à niveau n’est installée pour les visionneuses Image Serving. Adobe vous recommande de sauvegarder tout répertoire de lecteurs Dynamic Media (s7viewers) existant avant de poursuivre l’installation.

**Pour installer plusieurs visionneuses sur le même serveur :**

1. Renommez le fichier .war dans le contexte souhaité et déployez-le à l’emplacement souhaité.
1. Définissez le paramètre `this.isViewerRoot` dans `config.js`.
1. Ouvrez `config.js` à la racine du dossier du lecteur de contenu nouvellement créé.
1. Définissez le paramètre `this.isViewerRoot = "/s7viewers"` sur le contexte du fichier `s7viewers.war`. Par exemple, `"/s7viewers-4.0"`.
1. Enregistrez le fichier et fermez-le.
