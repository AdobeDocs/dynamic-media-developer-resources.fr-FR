---
description: Après avoir installé Image Serving sous Linux, vérifiez l’installation.
solution: Experience Manager
title: Vérification de l'installation
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Vérification de l&#39;installation{#verifying-the-installation}

Après avoir installé Image Serving sous Linux, vérifiez l’installation.

Le serveur d’images est installé en tant que démon Linux.

**Vérification de l’installation**

1. Vérifiez que le serveur d’images est configuré pour démarrer automatiquement et qu’il est en cours d’exécution :

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Vous devez disposer des autorisations racine pour exécuter ces scripts.

1. Ouvrez un navigateur Internet sur le même hôte ou sur un autre hôte et vérifiez la ou les réponses du serveur par défaut :

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

Dans les réponses, vérifiez la présence d’éléments commençant par &quot;`imageServer.`&quot;, qui indiquent que le serveur de plateforme a pu communiquer avec le serveur d’images.
>Une vérification supplémentaire peut être effectuée à l’aide des exemples de pages des packages Documentation et Demo , le cas échéant.
