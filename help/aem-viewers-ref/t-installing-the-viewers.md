---
description: Instructions d’installation de l’API des visionneuses Scene7.
seo-description: Instructions d’installation de l’API des visionneuses Scene7.
seo-title: Installation de plusieurs visionneuses sur le même serveur
solution: Experience Manager
title: Installation de plusieurs visionneuses sur le même serveur
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Installation de plusieurs visionneuses sur le même serveur{#installing-multiple-viewers-on-the-same-server}

Instructions d’installation de l’API des visionneuses Scene7.

Installez et testez Image Serving avant d’installer les visionneuses Image Serving.

Copiez les fichiers des visionneuses IS sur votre disque dur, puis déployez le `s7viewers.war` fichier dans le `../ImageServing/webapps` répertoire. Pour obtenir des instructions sur la manière de déployer, de , d’arrêter et de gérer le serveur Image Server, reportez-vous à la documentation de Image Serving.

>[!NOTE]
>
>Il n’existe aucune installation de mise à niveau pour les visionneuses de diffusion d’images. Adobe recommande de sauvegarder tout répertoire de visionneuses Scene7 existant avant de poursuivre l’installation.

**Pour installer les lecteurs sur le même serveur**

1. Renommez le fichier .war dans le contexte souhaité et déployez-le à l’emplacement souhaité.
1. Définissez `this.isViewerRoot` le paramètre dans `config.js`.
1. Ouvrez `config.js` situé à la racine du dossier du lecteur nouvellement créé.
1. Définissez le paramètre `this.isViewerRoot = "/s7viewers"` sur le contexte du `s7viewers.war` fichier. Par exemple, `"/s7viewers-4.0"`. Enregistrez et fermez le fichier.
1. Enregistrez le fichier et fermez-le.
