---
description: Après avoir installé Dynamic Media Image Serving, vous devez vérifier l’installation.
seo-description: Après avoir installé Dynamic Media Image Serving, vous devez vérifier l’installation.
seo-title: Vérification de l’installation
solution: Experience Manager
title: Vérification de l’installation
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '136'
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

