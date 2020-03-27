---
description: Les catalogues d’images fournissent de nombreux paramètres de configuration du serveur, ainsi que des polices, des  ICC et des macros de commande.
seo-description: Les catalogues d’images fournissent de nombreux paramètres de configuration du serveur, ainsi que des polices, des  ICC et des macros de commande.
seo-title: Catalogues d’images
solution: Experience Manager
title: Catalogues d’images
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Catalogues d’images{#image-catalogs}

Les catalogues d’images fournissent de nombreux paramètres de configuration du serveur, ainsi que des polices, des  ICC et des macros de commande.

Ils mappent les identifiants d’image et de contenu statique utilisés dans les requêtes aux chemins d’accès aux fichiers réels, stockent diverses métadonnées d’image, telles que les zones cliquables, et fournissent des  pour les modèles et les visionneuses d’images.

Les catalogues d’images sont accessibles uniquement par le serveur de plateformes et non par le serveur d’images. Les fichiers d’attributs de catalogue doivent avoir un suffixe .ini et être placés dans le dossier de catalogue du serveur de plateformes ( `PS::CatalogFolder`). Au moins, le catalogue d’images par défaut est requis et doit être renseigné avec tous les attributs pour le bon fonctionnement du serveur de plateformes.
