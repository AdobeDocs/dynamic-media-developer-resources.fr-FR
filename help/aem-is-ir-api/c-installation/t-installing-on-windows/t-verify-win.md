---
title: Vérification de l'installation
description: Après avoir installé Dynamic Media Image Serving, vous devez vérifier l’installation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Vérification de l&#39;installation {#verifying-the-installation}

Après avoir installé Dynamic Media Image Serving, vous devez vérifier l’installation.

Le serveur d’images est installé en tant que service Windows.

1. Ouvrez le Panneau de Contrôle Services et vérifiez que `Dynamic Media Image Serving` est présente avec un état de `Started`.
1. Ouvrez un navigateur Internet sur le même hôte ou sur un autre hôte et vérifiez les réponses du serveur par défaut :

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

Vérifiez la présence de &quot; `imageServer.`&quot; dans la réponse, qui indique que le serveur d’images écoute.
>Une vérification supplémentaire peut être effectuée à l’aide des exemples de pages des packages Documentation et Demo , le cas échéant.
