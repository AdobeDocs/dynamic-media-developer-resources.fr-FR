---
title: Vérification de l'installation
description: Après avoir installé la diffusion d’images sous Linux®, vérifiez l’installation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
TQID: 'https://experienceleague.adobe.com/LyHlwiFL1b-iwo1kSnUeNfNo3fZY6FZetHgnNFoxGZo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 0%

---

# Vérification de l&#39;installation{#verifying-the-installation}

Après avoir installé la diffusion d’images sous Linux®, vérifiez l’installation.

Image Server est installé en tant que démon Linux®.

**Pour vérifier l’installation**

1. Vérifiez que la Diffusion d’images est configurée pour démarrer automatiquement et qu’elle est en cours d’exécution :

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Vous devez disposer des autorisations de niveau racine pour exécuter ces scripts.

1. Ouvrez un navigateur Internet sur le même hôte ou sur un hôte différent et vérifiez les réponses du serveur par défaut :

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

Dans les réponses, recherchez la présence d’éléments commençant par `imageServer`, qui indiquent que l’[!DNL Platform Server] a pu communiquer avec le serveur d’images.

>Une vérification supplémentaire peut être effectuée à l’aide des exemples de pages des packages de documentation et de démonstration, le cas échéant.
