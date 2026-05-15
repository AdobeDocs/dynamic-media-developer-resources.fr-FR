---
title: Vérification de l'installation
description: Après avoir installé la diffusion d’images Dynamic Media, vous devez vérifier l’installation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
TQID: 'https://experienceleague.adobe.com/2i1-Ncy7lyIbm8BHFZGVLNIDnZUOA9sr3tZ970WswL4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# Vérification de l&#39;installation {#verifying-the-installation}

Après avoir installé la diffusion d’images Dynamic Media, vous devez vérifier l’installation.

Le serveur d’images est installé en tant que service Windows.

1. Ouvrez le Panneau de Contrôle Services et vérifiez que `Dynamic Media Image Serving` est présent avec le statut `Started`.
1. Ouvrez un navigateur Internet sur le même hôte ou sur un hôte différent et vérifiez les réponses du serveur par défaut :

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

Vérifiez la présence d’éléments « `imageServer.` » dans la réponse, qui indiquent que le serveur d’images écoute.

>Une vérification supplémentaire peut être effectuée à l’aide des exemples de pages des packages de documentation et de démonstration, le cas échéant.
