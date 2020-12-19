---
description: Le catalogue par défaut fournit des valeurs par défaut pour tous les attributs de catalogue pour tous les catalogues d’images.
seo-description: Le catalogue par défaut fournit des valeurs par défaut pour tous les attributs de catalogue pour tous les catalogues d’images.
seo-title: Catalogue par défaut
solution: Experience Manager
title: Catalogue par défaut
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f0c967e-a2fa-4ef0-bacb-3dcfb06a8027
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---


# Catalogue par défaut{#default-catalog}

Le catalogue par défaut fournit des valeurs par défaut pour tous les attributs de catalogue pour tous les catalogues d’images.

Si un attribut spécifique est introuvable dans un catalogue d’images spécifique, le serveur utilise à la place la valeur correspondante du catalogue par défaut. De même, le catalogue par défaut peut être utilisé pour fournir des valeurs par défaut pour des enregistrements de données de catalogue spécifiques (images, définitions de macro, polices et profils ICC). Si un enregistrement de données spécifique est introuvable dans un catalogue d’images spécifique, le serveur tente plutôt de le trouver dans le catalogue par défaut. Cela permet aux catalogues d’images d’être peu renseignés et simplifie la gestion des attributs et données globaux, tels que les modèles partagés, les macros, les polices, etc.

En outre, le catalogue par défaut fournit tous les attributs et enregistrements de données (macros, polices, profils ICC, demander des règles de prétraitement) lorsqu’aucun catalogue d’images spécifique n’est impliqué dans une opération.

Pour que le serveur de plateformes fonctionne correctement, le fichier d&#39;attributs de catalogue du catalogue par défaut doit être nommé [!DNL default.ini], doit toujours exister dans le dossier de catalogue et doit être entièrement renseigné avec tous les attributs requis, à l&#39;exclusion de `attribute::RootId` et des références aux différents fichiers de données de catalogue, qui sont tous facultatifs.

>[!NOTE]
>
>Tous les fichiers d&#39;attributs de catalogue, à l&#39;exception de [!DNL default.ini], doivent contenir une valeur `attribute::RootId` unique. `attribute::RootId` dans  [!DNL default.ini] doit être vide.

