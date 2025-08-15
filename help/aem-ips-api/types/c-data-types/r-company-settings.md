---
description: Paramètres de configuration spécifiques à l’entreprise.
solution: Experience Manager
title: Paramètres de la société
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 2%

---

# [!DNL CompanySettings]{#companysettings}

Paramètres de configuration spécifiques à l’entreprise.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| Mode de remplacement | `xsd:string` | Détermine s’il faut écraser les images du dossier actif avec le même nom et la même extension d’image de base. |
| retainPublishState | `xsd:boolean` | Spécifie si une image de remplacement téléchargée dans IPS doit conserver le paramètre existant « Prêt à Publish » ou s’il doit être tel que spécifié par le téléchargement. |
| Profil par défaut | `types:Asset` | Spécifie le profil de couleurs source par défaut (Coated FOGRA27 (ISO 126472:2004)) appliqué automatiquement dans le cadre de l’utilisation du comportement de couleur par défaut lors de l’ajout de fichiers image CMJN. |
| Profil d’affichage par défaut | `types:Asset` | Spécifie le profil de couleurs interne par défaut (U.S. Web Coated (SWOP) v2) automatiquement appliqué dans le cadre de l’option « Utiliser le comportement des couleurs par défaut » lors de l’ajout de fichiers image CMJN. |
| iptcExifMappingXslt | `types:Asset` | L’extraction des données d’en-tête d’image IPTC et EXIF en IPS nécessite une conversion des noms de champ internes en noms de champs définis par l’utilisateur pour la société. Détermine une table de traduction XSL (la valeur par défaut est « Ne pas extraire de champs IPTC ou EXIF ») pour les images chargées. |
| xmpMappingXslt | `types:Asset` | L’extraction de XMP données d’en-tête d’image dans IPS nécessite une conversion des noms de champ internes en noms de champ définis par l’utilisateur pour la société. Détermine une table de conversion XSL (la valeur par défaut est « Ne pas extraire de champs XMP ») pour les images chargées. |
| Avertissement de l’espace de disque | `xsd:int` | Quantité minimale d’espace disque disponible dans le répertoire d’images avant l’envoi d’un avertissement. |
| EmailTrashCleanupWarning | `xsd:boolean` | Détermine s’il faut envoyer des e-mails avant que les éléments de la corbeille ne soient automatiquement supprimés. |
| JavaScriptUploadEnabled | `types:Asset` | Détermine si les fichiers d’JavaScript doivent être téléchargés. Cette option présente un risque potentiel pour la sécurité, alors utilisez-la avec précaution. |
