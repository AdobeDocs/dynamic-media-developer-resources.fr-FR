---
title: Présentation du catalogue de matières
description: Les catalogues de matériaux fournissent au serveur des informations sur les vignettes, le matériel et les données annexes, telles que les profils ICC.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d26371da-e992-4f63-a5be-190ce60eca2f
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Présentation du catalogue de matières{#material-catalog-overview}

Les catalogues de matériaux fournissent au serveur des informations sur les vignettes, le matériel et les données annexes, telles que les profils ICC.

Chaque catalogue de matériaux se compose d’un *fichier d’attribut de catalogue* requis et d’un ensemble de *fichiers de données de catalogue* facultatifs :

* Le fichier de mappage de vignettes, qui énumère les vignettes, les modèles et leurs métadonnées associées.
* Le fichier de données de matériau, qui énumère les matériaux et spécifie les fichiers d’image et les métadonnées de texture associés.
* Le fichier de définitions de macro qui fournit des définitions pour les macros de requête.
* Le fichier de mappage de profil, qui énumère les profils de couleurs ICC.

Les fichiers de données de catalogue sont associés à des catalogues de matériaux par référence de fichier dans le fichier d’attributs de catalogue. Le même fichier de données de catalogue peut être partagé par plusieurs catalogues de matériaux.

Les fichiers d’attributs du catalogue doivent avoir un suffixe de fichier [!DNL `.ini`] et se trouver dans le *dossier catalogue* de rendu d’image ( [!DNL PlatformServer::ir.catalogRootPath]). Les fichiers de données du catalogue peuvent se trouver dans le même dossier ou tout autre dossier accessible au serveur de rendu.

**Mise à jour des catalogues de matériaux**

Le serveur surveille en permanence le dossier de catalogue. Il recharge automatiquement un catalogue de matières, y compris les fichiers de données de catalogue associés, lorsqu’il détecte que le fichier d’attribut du catalogue principal a été modifié. Ainsi, pour mettre à jour les catalogues de matériaux sur le serveur, vous devez d’abord remplacer tous les fichiers de données de catalogue qui doivent être modifiés, puis remplacer (ou &quot;toucher&quot;) le fichier d’attributs de catalogue pour déclencher le rechargement du catalogue.

**Catalogue par défaut**

Le catalogue par défaut fournit des valeurs par défaut pour tous les attributs de catalogue pour tous les catalogues de matériaux. Si un attribut particulier est introuvable dans un catalogue de matières spécifique, le serveur utilise la valeur correspondante du catalogue par défaut à la place. De même, le catalogue par défaut peut être utilisé pour fournir des valeurs par défaut pour des enregistrements de données de catalogue spécifiques (matériaux et profils ICC). Si un enregistrement de données spécifique est introuvable dans un catalogue de matières spécifique, le serveur tente plutôt de le trouver dans le catalogue par défaut. Cela permet de peu remplir les catalogues de matériaux et simplifie la gestion des attributs et données globaux, tels que les modèles, les macros et les polices partagées.

En outre, le catalogue par défaut fournit tous les attributs et enregistrements de données (profils ICC) lorsqu’aucun catalogue de matériel spécifique n’est impliqué dans une opération.

Pour que le serveur de rendu fonctionne correctement, le fichier d’attributs de catalogue du catalogue par défaut doit être nommé [!DNL default.ini]. Il doit également toujours exister dans le dossier de catalogue et doit être entièrement renseigné avec tous les attributs requis, à l’exception de `attribute::RootId` et des références aux différents fichiers de données de catalogue, qui sont tous facultatifs.

<!-- **See also**

`PlatformServer::ir.catalogRootPath` -->
