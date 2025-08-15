---
description: Les catalogues d’images fournissent de nombreux paramètres de configuration du serveur, ainsi que des polices, des profils ICC et des macros de commande.
solution: Experience Manager
title: Catalogues d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Catalogues d’images{#image-catalogs}

Les catalogues d’images fournissent de nombreux paramètres de configuration du serveur, ainsi que des polices, des profils ICC et des macros de commande.

Ils mappent les identifiants d’image et de contenu statique utilisés dans les requêtes aux chemins d’accès de fichiers réels, stockent diverses métadonnées d’image, telles que les zones cliquables, et fournissent des conteneurs pour les modèles et les visionneuses d’images.

Les catalogues d’images ne sont accessibles que par le [!DNL Platform Server], et jamais par le serveur d’images. Les fichiers d’attributs de catalogue doivent comporter un suffixe .ini et être placés dans le dossier de catalogue du [!DNL Platform Server] ( `PS::CatalogFolder`). Le catalogue d’images par défaut est au moins obligatoire et doit être renseigné avec tous les attributs pour un fonctionnement correct du [!DNL Platform Server].
