---
title: Installation de plusieurs visionneuses Dynamic Media sur le même serveur
description: Instructions d’installation de l’API Visionneuses Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Visionneuses,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# Installation de plusieurs visionneuses sur le même serveur{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instructions d’installation de l’API des visionneuses Dynamic Media.

Installez et testez Image Serving avant d’installer les visionneuses Image Serving.

Copiez les fichiers Visionneuses IS sur votre disque dur, puis déployez le fichier `s7viewers.war` dans le répertoire `../ImageServing/webapps`. Pour plus d’informations sur le déploiement, le démarrage, l’arrêt et la gestion du serveur d’images, reportez-vous à la documentation relative au serveur d’images .

>[!NOTE]
>
>Il n’existe aucune installation de mise à niveau pour les visionneuses Image Serving. Adobe vous recommande de sauvegarder tous les répertoires de visionneuses Dynamic Media (s7viewers) existants avant de poursuivre l’installation.

**Pour installer plusieurs visionneuses sur le même serveur :**

1. Renommez la visionneuse .war en fonction du contexte souhaité et déployez le fichier à l’emplacement de votre choix.
1. Définissez le paramètre `this.isViewerRoot` dans `config.js`.
1. Ouvrez `config.js` à la racine du dossier de visionneuse nouvellement créé.
1. Définissez le paramètre `this.isViewerRoot = "/s7viewers"` sur le contexte du fichier `s7viewers.war`. Par exemple, `"/s7viewers-4.0"`.
1. Enregistrez le fichier et fermez-le.
