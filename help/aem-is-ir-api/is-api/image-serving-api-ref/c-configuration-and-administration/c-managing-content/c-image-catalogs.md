---
description: Les catalogues d’images offrent de nombreux paramètres de configuration de serveur, ainsi que des polices, des profils ICC et des macros de commande.
solution: Experience Manager
title: Catalogues d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# Catalogues d’images{#image-catalogs}

Les catalogues d’images offrent de nombreux paramètres de configuration de serveur, ainsi que des polices, des profils ICC et des macros de commande.

Ils mappent les identifiants d’image et de contenu statique utilisés dans les requêtes aux chemins d’accès aux fichiers réels, stockent diverses métadonnées d’image, telles que les zones cliquables, et fournissent des conteneurs pour les modèles et les visionneuses d’images.

Les catalogues d’images sont accessibles uniquement par le serveur de plateformes, et non par le serveur d’images. Les fichiers d’attributs du catalogue doivent avoir un suffixe .ini et être placés dans le dossier de catalogue de Platform Server ( `PS::CatalogFolder`). Au moins, le catalogue d’images par défaut est requis et doit être renseigné avec tous les attributs pour le bon fonctionnement de Platform Server.
