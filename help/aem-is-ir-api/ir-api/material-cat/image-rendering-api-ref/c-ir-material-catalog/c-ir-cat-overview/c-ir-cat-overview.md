---
description: Les catalogues de matériaux fournissent au serveur des informations sur les vignettes, les matériaux et les données de prise en charge, telles que les profils ICC.
solution: Experience Manager
title: Présentation du catalogue de matières *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---


# Présentation du catalogue de matières *{#material-catalog-overview}

Les catalogues de matériaux fournissent au serveur des informations sur les vignettes, les matériaux et les données de prise en charge, telles que les profils ICC.

Chaque catalogue de matières est constitué d&#39;un *fichier d&#39;attribut de catalogue* obligatoire et d&#39;un ensemble de *fichiers de données de catalogue* facultatifs :

* Le fichier de mappage de vignettes, qui répertorie les vignettes et les modèles et leurs métadonnées associées.
* Le fichier de données de matériau, qui permet d’itétrer les matériaux et de spécifier les fichiers d’image de texture et les métadonnées associées.
* Fichier de définitions de macro qui fournit des définitions pour les macros de demande.
* Le fichier de mappage de profil, qui répertorie les profils de couleur ICC.

Les fichiers de données de catalogue sont associés à des catalogues de matières par référence de fichier dans le fichier d’attribut de catalogue. Le même fichier de données de catalogue peut être partagé par plusieurs catalogues de matières.

Les fichiers d’attributs du catalogue doivent avoir un suffixe de fichier [!DNL .ini] et être situés dans le dossier de catalogue de rendu d’image ** ( [!DNL PlatformServer::ir.catalogRootPath]). Les fichiers de données de catalogue peuvent se trouver dans le même dossier ou dans tout autre dossier accessible au serveur de rendu.

**Mise à jour des catalogues de matières**

Le serveur surveille en permanence le dossier de catalogue et recharge automatiquement un catalogue de matières, y compris les fichiers de données de catalogue associés, lorsqu’il détecte que le fichier d’attribut de catalogue principal a été modifié. Ainsi, pour mettre à jour les catalogues de matériaux sur le serveur, vous devez d’abord remplacer tous les fichiers de données de catalogue qui doivent être modifiés, puis remplacer (ou &quot;toucher&quot;) le fichier d’attributs de catalogue pour déclencher le rechargement du catalogue.

**Catalogue par défaut**

Le catalogue par défaut fournit des valeurs par défaut pour tous les attributs de catalogue pour tous les catalogues de matières. Si un attribut spécifique est introuvable dans un catalogue de matières spécifique, le serveur utilisera plutôt la valeur correspondante du catalogue par défaut. De même, le catalogue par défaut peut être utilisé pour fournir des valeurs par défaut pour des enregistrements de données de catalogue spécifiques (matériaux et profils ICC). Si un enregistrement de données spécifique est introuvable dans un catalogue de matières spécifique, le serveur tentera plutôt de le trouver dans le catalogue par défaut. Cela permet aux catalogues de matériaux d’être peu renseignés et simplifie la gestion des attributs et données globaux, tels que les modèles partagés, les macros, les polices, etc.

En outre, le catalogue par défaut fournit tous les attributs et enregistrements de données (profils ICC) lorsqu’aucun catalogue de matières spécifique n’est impliqué dans une opération.

Pour que le serveur de rendu fonctionne correctement, le fichier d&#39;attributs du catalogue pour le catalogue par défaut doit être nommé [!DNL default.ini], doit toujours exister dans le dossier de catalogue et doit être entièrement renseigné avec tous les attributs requis, à l&#39;exclusion de `attribute::RootId` et des références aux différents fichiers de données du catalogue, qui sont tous facultatifs.

**Voir aussi**

`PlatformServer::ir.catalogRootPath`
