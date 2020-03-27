---
description: Les catalogues de matériaux fournissent au serveur des informations sur les vignettes, les matériaux et les données de prise en charge, telles que les  ICC.
seo-description: Les catalogues de matériaux fournissent au serveur des informations sur les vignettes, les matériaux et les données de prise en charge, telles que les  ICC.
seo-title: Présentation du catalogue de matières *
solution: Experience Manager
title: Présentation du catalogue de matières *
topic: Scene7 Image Serving - Image Rendering API
uuid: f2128b64-8caf-4a59-b11f-604fe62bae69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Présentation du catalogue de matières *{#material-catalog-overview}

Les catalogues de matériaux fournissent au serveur des informations sur les vignettes, les matériaux et les données de prise en charge, telles que les  ICC.

Chaque catalogue de matières se compose d’un fichier *d’attributs de* catalogue requis et d’un ensemble de fichiers *de données de* catalogue facultatifs :

* Le fichier de mappage de vignettes, qui répertorie les vignettes et les modèles et leurs métadonnées associées.
* Le fichier de données de matériau, qui répertorie les matériaux et spécifie les fichiers d’image de texture et les métadonnées associés.
* Fichier de définitions de macro, qui fournit des définitions pour les macros de demande.
* Le fichier de mappage , qui répertorie les de couleurs ICC .

Les fichiers de données de catalogue sont associés aux catalogues de matériaux par référence à un fichier dans le fichier d’attribut de catalogue. Le même fichier de données de catalogue peut être partagé par plusieurs catalogues de matières.

Les fichiers d’attribut de catalogue doivent avoir un suffixe de [!DNL .ini] fichier et se trouver dans le dossier *du* catalogue de rendu d’image ( [!DNL PlatformServer::ir.catalogRootPath]). Les fichiers de données de catalogue peuvent se trouver dans le même dossier ou dans tout autre dossier accessible au serveur de rendu.

**Mise à jour des catalogues de matériaux**

Le serveur surveille en permanence le dossier du catalogue et recharge automatiquement un catalogue de matières, y compris les fichiers de données de catalogue associés, lorsqu’il détecte que le fichier d’attribut de catalogue principal a été modifié. Ainsi, pour mettre à jour les catalogues de matériaux sur le serveur, remplacez d’abord tous les fichiers de données de catalogue qui doivent être modifiés, puis remplacez (ou &quot;appuyez&quot;) le fichier d’attributs de catalogue pour déclencher le rechargement du catalogue.

**Catalogue par défaut**

Le catalogue par défaut fournit des valeurs par défaut pour tous les attributs de catalogue pour tous les catalogues de matières. Si un attribut spécifique est introuvable dans un catalogue de matériaux spécifique, le serveur utilisera plutôt la valeur correspondante du catalogue par défaut. De même, le catalogue par défaut peut être utilisé pour fournir des valeurs par défaut pour des enregistrements de données de catalogue spécifiques (matériaux et  ICC). Si un enregistrement de données spécifique est introuvable dans un catalogue de matières spécifique, le serveur tentera plutôt de le trouver dans le catalogue par défaut. Cela permet aux catalogues de matériaux d’être peu renseignés et simplifie la gestion des attributs et des données globaux, tels que les modèles partagés, les macros, les polices, etc.

En outre, le catalogue par défaut fournit tous les attributs et enregistrements de données (ICC) lorsqu’aucun catalogue de matières spécifique n’est impliqué dans une opération.

Pour que le serveur de rendu fonctionne correctement, le fichier d’attributs de catalogue du catalogue par défaut doit être nommé [!DNL default.ini], doit toujours exister dans le dossier de catalogue et doit être entièrement renseigné avec tous les attributs requis, à l’exclusion `attribute::RootId` et des références aux différents fichiers de données de catalogue, qui sont tous facultatifs.

**Voir aussi**

`PlatformServer::ir.catalogRootPath`
