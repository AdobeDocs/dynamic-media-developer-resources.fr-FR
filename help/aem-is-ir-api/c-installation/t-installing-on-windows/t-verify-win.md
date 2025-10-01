---
title: Vérification de l'installation
description: Après avoir installé la diffusion d’images Dynamic Media, vous devez vérifier l’installation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Vérification de l&#39;installation {#verifying-the-installation}

Après avoir installé la diffusion d’images Dynamic Media, vous devez vérifier l’installation.

Le serveur d’images est installé en tant que service Windows.

1. Ouvrez le Panneau de Contrôle Services et vérifiez que `Dynamic Media Image Serving` est présent avec le statut `Started`.
1. Ouvrez un navigateur Internet sur le même hôte ou sur un hôte différent et vérifiez les réponses du serveur par défaut :

   `http:// server:port /is/image`

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

Vérifiez la présence d’éléments « `imageServer.` » dans la réponse, qui indiquent que le serveur d’images écoute.

>Une vérification supplémentaire peut être effectuée à l’aide des exemples de pages des packages de documentation et de démonstration, le cas échéant.
