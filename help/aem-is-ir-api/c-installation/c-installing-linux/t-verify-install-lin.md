---
title: Vérification de l'installation
description: Après avoir installé Image Serving sous Linux®, vérifiez l’installation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# Vérification de l&#39;installation{#verifying-the-installation}

Après avoir installé Image Serving sous Linux®, vérifiez l’installation.

Le serveur d’images est installé en tant que démon Linux®.

**Vérification de l’installation**

1. Vérifiez que le serveur d’images est configuré pour démarrer automatiquement et qu’il est en cours d’exécution :

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Vous devez disposer des autorisations racine pour exécuter ces scripts.

1. Ouvrez un navigateur Internet sur le même hôte ou sur un autre hôte et vérifiez les réponses du serveur par défaut :

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

Dans les réponses, vérifiez la présence d’éléments commençant par `imageServer`, qui indiquent que le serveur Platform a réussi à communiquer avec le serveur d’images.

>Une vérification supplémentaire peut être effectuée à l’aide des exemples de pages des packages Documentation et Demo , le cas échéant.
