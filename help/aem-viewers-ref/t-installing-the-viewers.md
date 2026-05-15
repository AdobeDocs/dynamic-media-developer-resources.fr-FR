---
title: Installation de plusieurs visionneuses Dynamic Media sur le même serveur
description: Instructions d’installation de l’API Visionneuses Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
TQID: 'https://experienceleague.adobe.com/Zz0BTc333AIELPKRWFeIxhNvTyOJZH1RHLYNvZpt-ZY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 0%

---

# Installation de plusieurs visionneuses sur le même serveur{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instructions d’installation de l’API des visionneuses Dynamic Media.

Installez et testez la diffusion d’images avant d’installer les visionneuses de diffusion d’images.

Copiez les fichiers de visionneuses IS sur votre disque dur, puis déployez le fichier `s7viewers.war` dans le répertoire `../ImageServing/webapps`. Consultez la documentation de votre hébergeur d’images pour obtenir des instructions sur le déploiement, le démarrage, l’arrêt et la gestion du serveur d’images.

>[!NOTE]
>
>Il n’existe aucune installation de mise à niveau pour les visionneuses de diffusion d’images. Adobe vous recommande de sauvegarder tout répertoire existant des visionneuses Dynamic Media (s7viewers) avant de poursuivre l’installation.

**Pour installer plusieurs visionneuses sur le même serveur, procédez comme suit**

1. Renommez le fichier war de la visionneuse dans le contexte souhaité et déployez-le à l’emplacement souhaité.
1. Définissez `this.isViewerRoot` paramètre dans `config.js`.
1. Ouvrez `config.js` à la racine du dossier de visionneuse que vous venez de créer.
1. Définissez le paramètre `this.isViewerRoot = "/s7viewers"` sur le contexte du fichier `s7viewers.war`. Par exemple, `"/s7viewers-4.0"`.
1. Enregistrez le fichier et fermez.
