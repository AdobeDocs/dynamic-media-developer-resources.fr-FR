---
description: Après avoir installé Image Serving sur Linux, vérifiez l’installation.
solution: Experience Manager
title: Vérification de l’installation
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '137'
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

