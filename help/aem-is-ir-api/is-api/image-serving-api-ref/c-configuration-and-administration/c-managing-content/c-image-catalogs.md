---
description: Les catalogues d’images fournissent de nombreux paramètres de configuration du serveur, ainsi que les polices, les profils ICC et les macros de commande.
solution: Experience Manager
title: Catalogues d’images
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# Catalogues d’images{#image-catalogs}

Les catalogues d’images fournissent de nombreux paramètres de configuration du serveur, ainsi que les polices, les profils ICC et les macros de commande.

Ils mappent les identifiants d’image et de contenu statique utilisés dans les demandes aux chemins d’accès aux fichiers réels, stockent diverses métadonnées d’image, telles que les zones cliquables, et fournissent des conteneurs pour les modèles et les visionneuses d’images.

Les catalogues d’images sont accessibles uniquement par le serveur Platform, et jamais par le serveur d’images. Les fichiers d’attributs du catalogue doivent comporter le suffixe .ini et être placés dans le dossier de catalogue du serveur de plateformes ( `PS::CatalogFolder`). Au moins, le catalogue d’images par défaut est requis et doit être renseigné avec tous les attributs pour le bon fonctionnement de Platform Server.
