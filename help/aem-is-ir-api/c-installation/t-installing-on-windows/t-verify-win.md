---
description: Après avoir installé Dynamic Media Image Serving, vous devez vérifier l’installation.
solution: Experience Manager
title: Vérification de l'installation
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Vérification de l&#39;installation{#verifying-the-installation}

Après avoir installé Dynamic Media Image Serving, vous devez vérifier l’installation.

Le serveur d’images est installé en tant que service Windows.

1. Ouvrez le Panneau de Contrôle Services et vérifiez que &quot;Dynamic Media Image Serving&quot; est présent avec le statut &quot;Démarré&quot;.
1. Ouvrez un navigateur Internet sur le même hôte ou sur un autre hôte et vérifiez les réponses du serveur par défaut :

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

Vérifiez la présence d’éléments &quot; `imageServer.`&quot; dans la réponse, qui indiquent que le serveur d’images écoute.
>Une vérification supplémentaire peut être effectuée à l’aide des exemples de pages des packages Documentation et Demo , le cas échéant.
