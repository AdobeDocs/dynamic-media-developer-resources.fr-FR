---
description: Le catalogue par défaut fournit des valeurs par défaut pour tous les attributs de catalogue pour tous les catalogues d’images.
solution: Experience Manager
title: Catalogue par défaut
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Catalogue par défaut{#default-catalog}

Le catalogue par défaut fournit des valeurs par défaut pour tous les attributs de catalogue pour tous les catalogues d’images.

Si un attribut particulier est introuvable dans un catalogue d’images spécifique, le serveur utilise la valeur correspondante du catalogue par défaut à la place. De même, le catalogue par défaut peut être utilisé pour fournir des valeurs par défaut pour des enregistrements de données de catalogue spécifiques (images, définitions de macro, polices et profils ICC). Si un enregistrement de données spécifique est introuvable dans un catalogue d’images spécifique, le serveur tente plutôt de le trouver dans le catalogue par défaut. Cela permet de peu remplir les catalogues d’images et simplifie la gestion des attributs et données globaux, tels que les modèles partagés, les macros, les polices, etc.

En outre, le catalogue par défaut fournit tous les attributs et enregistrements de données (macros, polices, profils ICC, règles de prétraitement des demandes) lorsqu’aucun catalogue d’images spécifique n’est impliqué dans une opération.

Pour que le serveur Platform fonctionne correctement, le fichier d’attributs du catalogue pour le catalogue par défaut doit être nommé [!DNL default.ini], doit toujours exister dans le dossier du catalogue et doit être entièrement renseigné avec tous les attributs requis, à l’exclusion de `attribute::RootId` et les références aux différents fichiers de données du catalogue, qui sont tous facultatifs.

>[!NOTE]
>
>Tous les fichiers d’attributs du catalogue à l’exception de [!DNL default.ini] doivent contenir une valeur `attribute::RootId` unique. `attribute::RootId` dans  [!DNL default.ini] doit être vide.
