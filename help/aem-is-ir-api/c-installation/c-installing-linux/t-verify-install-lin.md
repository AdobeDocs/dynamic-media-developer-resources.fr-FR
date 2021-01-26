---
description: Après avoir installé Image Serving sur Linux, vérifiez l’installation.
seo-description: Après avoir installé Image Serving sur Linux, vérifiez l’installation.
seo-title: Vérification de l’installation
solution: Experience Manager
title: Vérification de l’installation
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---


# Vérification de l’installation{#verifying-the-installation}

Après avoir installé Image Serving sur Linux, vérifiez l’installation.

Image Server est installé en tant que démon Linux.

**Pour vérifier l’installation**

1. Vérifiez que la diffusion d’images est configurée pour le début automatiquement et qu’elle est en cours d’exécution :

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Vous devez disposer des autorisations racine pour exécuter ces scripts.

1. Ouvrez un navigateur Internet sur le même hôte ou sur un hôte différent et vérifiez les réponses du serveur par défaut :

[ ! DNL http:// *[!DNL server:port]*/is/image]

[ ! DNL http:// *[!DNL server:port]*/ir/render]

Dans les réponses, vérifiez la présence d’éléments commençant par &quot; `imageServer.`&quot;, qui indiquent que le serveur de plateformes a pu communiquer avec le serveur d’images.
>Une vérification supplémentaire peut être effectuée à l’aide des exemples de pages des packages Documentation et Démo, le cas échéant.

