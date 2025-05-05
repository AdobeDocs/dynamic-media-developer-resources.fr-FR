---
title: Vérification de l'installation
description: Après avoir installé Image Serving sous Linux®, vérifiez l’installation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Vérification de l&#39;installation{#verifying-the-installation}

Après avoir installé Image Serving sous Linux®, vérifiez l’installation.

Le serveur d’images est installé en tant que démon Linux®.

**Pour vérifier l’installation**

1. Vérifiez que le serveur d’images est configuré pour démarrer automatiquement et qu’il est en cours d’exécution :

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Vous devez disposer des autorisations racine pour exécuter ces scripts.

1. Ouvrez un navigateur Internet sur le même hôte ou sur un autre hôte et vérifiez les réponses du serveur par défaut :

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

Dans les réponses, vérifiez la présence d’éléments commençant par `imageServer`, qui indiquent que [!DNL Platform Server] a pu communiquer avec le serveur d’images.

>Une vérification supplémentaire peut être effectuée à l’aide des exemples de pages des packages Documentation et Demo , le cas échéant.
