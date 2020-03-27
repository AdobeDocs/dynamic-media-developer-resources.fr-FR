---
description: Après avoir installé Scene7 Image Serving, vérifiez l’installation.
seo-description: Après avoir installé Scene7 Image Serving, vérifiez l’installation.
seo-title: Vérification de l’installation
solution: Experience Manager
title: Vérification de l’installation
topic: Scene7 Image Serving - Image Rendering API
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Vérification de l’installation{#verifying-the-installation}

Après avoir installé Scene7 Image Serving, vérifiez l’installation.

Image Server est installé en tant que service Windows.

1. Ouvrez le Panneau de configuration des services et vérifiez que &quot;Scene7 Image Serving&quot; est présent avec l’état &quot;Démarré&quot;.
1. Ouvrez un navigateur Internet sur le même hôte ou sur un hôte différent et vérifiez les réponses du serveur par défaut :

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

Vérifiez la présence des éléments &quot; `imageServer.`&quot; dans la réponse, qui indiquent que le serveur d’images écoute.
>Une vérification supplémentaire peut être effectuée à l’aide des exemples de pages des packages Documentation et Démo, le cas échéant.

