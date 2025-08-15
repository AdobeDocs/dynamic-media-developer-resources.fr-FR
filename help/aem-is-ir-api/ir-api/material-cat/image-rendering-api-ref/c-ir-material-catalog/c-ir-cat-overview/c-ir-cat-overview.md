---
title: Présentation du catalogue de matières
description: Les catalogues de matériaux fournissent au serveur des informations sur les vignettes, les matériaux et les données de support, telles que les profils ICC.
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

Les catalogues de matériaux fournissent au serveur des informations sur les vignettes, les matériaux et les données de support, telles que les profils ICC.

Chaque catalogue de matières se compose d&#39;un *fichier d&#39;attributs de catalogue* obligatoire et d&#39;un ensemble de *fichiers de données de catalogue* facultatifs :

* Le fichier de mappage des vignettes, qui énumère les vignettes et les modèles, ainsi que les métadonnées qui leur sont associées.
* Le fichier de données des matériaux, qui détaille les matériaux et spécifie les fichiers d&#39;image et les métadonnées de texture associés.
* Le fichier de définitions de macro, qui fournit des définitions pour les macros de requête.
* Le fichier de mappage de profils qui énumère les profils de couleurs ICC.

Les fichiers de données de catalogue sont associés aux catalogues de matières par des références de fichier dans le fichier d&#39;attributs de catalogue. Le même fichier de données de catalogue peut être partagé par plusieurs catalogues de matériaux.

Les fichiers d’attributs de catalogue doivent comporter un suffixe de fichier [!DNL `.ini`] et se trouver dans le rendu d’images *dossier du catalogue* ( [!DNL PlatformServer::ir.catalogRootPath]). Les fichiers de données du catalogue peuvent se trouver dans le même dossier ou dans tout autre dossier accessible au serveur de rendu.

**Mise à jour des catalogues de matières**

Le serveur surveille en permanence le dossier de catalogue. Il recharge automatiquement un catalogue de matières, y compris les fichiers de données de catalogue associés, lorsqu&#39;il détecte que le fichier d&#39;attributs de catalogue principal a été modifié. Ainsi, pour mettre à jour les catalogues de matières sur le serveur, remplacez d’abord tous les fichiers de données de catalogue qui doivent être modifiés, puis remplacez (ou « touchez ») le fichier d’attributs de catalogue pour déclencher le rechargement du catalogue.

**Catalogue par défaut**

Le catalogue par défaut fournit des valeurs par défaut pour tous les attributs de catalogue de tous les catalogues de matières. Si un attribut particulier est introuvable dans un catalogue de matières spécifique, le serveur utilise la valeur correspondante du catalogue par défaut à la place. De même, le catalogue par défaut peut être utilisé pour fournir des valeurs par défaut pour des enregistrements de données de catalogue spécifiques (matériaux et profils ICC). Si un enregistrement de données particulier est introuvable dans un catalogue de matières spécifique, le serveur tente de le trouver dans le catalogue par défaut. Cela permet de renseigner les catalogues de matériaux de manière éparse et de simplifier la gestion des attributs et des données globaux, tels que les modèles partagés, les macros et les polices.

En outre, le catalogue par défaut fournit tous les attributs et enregistrements de données (profils ICC) lorsqu&#39;aucun catalogue de matières spécifique n&#39;est impliqué dans une opération.

Pour que le serveur de rendu fonctionne correctement, le fichier d’attributs de catalogue du catalogue par défaut doit être nommé [!DNL default.ini]. Il doit également toujours exister dans le dossier de catalogue et doit être entièrement renseigné avec tous les attributs requis, à l’exclusion des `attribute::RootId` et des références aux différents fichiers de données de catalogue, qui sont tous facultatifs.

<!-- **See also**

`PlatformServer::ir.catalogRootPath` -->
