---
description: Après avoir installé Dynamic Media Image Serving, vous devez vérifier l’installation.
seo-description: Après avoir installé Dynamic Media Image Serving, vous devez vérifier l’installation.
seo-title: Vérification de l’installation
solution: Experience Manager
title: Vérification de l’installation
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Vérification de l’installation{#verifying-the-installation}

Après avoir installé Dynamic Media Image Serving, vous devez vérifier l’installation.

Image Server est installé en tant que service Windows.

1. Ouvrez le Panneau de Contrôle Services et vérifiez que &quot;Dynamic Media Image Serving&quot; est présent avec l’état &quot;Started&quot; (Démarré).
1. Ouvrez un navigateur Internet sur le même hôte ou sur un hôte différent et vérifiez les réponses du serveur par défaut :

   `http:// server:port /is/image`

[ ! DNL http:// *[!DNL server:port]*/ir/render]

Vérifiez la présence des éléments &quot; `imageServer.`&quot; dans la réponse, qui indiquent que le serveur d’images écoute.
>Une vérification supplémentaire peut être effectuée à l’aide des exemples de pages des packages Documentation et Démo, le cas échéant.

