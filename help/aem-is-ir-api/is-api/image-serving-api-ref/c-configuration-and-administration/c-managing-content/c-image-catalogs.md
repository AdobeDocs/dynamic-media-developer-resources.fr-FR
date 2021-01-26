---
description: Les catalogues d’images offrent de nombreux paramètres de configuration de serveur, ainsi que des polices, des profils ICC et des macros de commande.
seo-description: Les catalogues d’images offrent de nombreux paramètres de configuration de serveur, ainsi que des polices, des profils ICC et des macros de commande.
seo-title: Catalogues d’images
solution: Experience Manager
title: Catalogues d’images
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# Catalogues d’images{#image-catalogs}

Les catalogues d’images offrent de nombreux paramètres de configuration de serveur, ainsi que des polices, des profils ICC et des macros de commande.

Ils mappent les identifiants d’image et de contenu statique utilisés dans les requêtes aux chemins d’accès aux fichiers réels, stockent diverses métadonnées d’image, telles que les zones cliquables, et fournissent des conteneurs pour les modèles et les visionneuses d’images.

Les catalogues d’images sont accessibles uniquement par le serveur de plateformes, et non par le serveur d’images. Les fichiers d’attributs du catalogue doivent avoir un suffixe .ini et être placés dans le dossier de catalogue de Platform Server ( `PS::CatalogFolder`). Au moins, le catalogue d’images par défaut est requis et doit être renseigné avec tous les attributs pour le bon fonctionnement de Platform Server.
