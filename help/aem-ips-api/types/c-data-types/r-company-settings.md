---
description: Paramètres de configuration spécifiques à l’entreprise.
solution: Experience Manager
title: Paramètres de la société
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 2%

---

# Paramètres de la société{#companysettings}

Paramètres de configuration spécifiques à l’entreprise.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`overwriteMode`*` | `xsd:string` | Détermine s’il faut remplacer les images du dossier actuel par le même nom et la même extension d’image de base. |
| `*`keepPublishState`*` | `xsd:boolean` | Indique si une image de remplacement chargée dans IPS doit conserver le paramètre &quot;Prêt à publier&quot; existant ou si elle doit être spécifiée par le téléchargement. |
| `*`defaultSourceProfile`*` | `types:Asset` | Indique le profil colorimétrique source par défaut (Coated FOGRA27 (ISO 126472:2004)) automatiquement appliqué dans le cadre du &quot;comportement par défaut des couleurs&quot; lors de l’ajout de fichiers image CMJN. |
| `*`defaultDisplayProfile`*` | `types:Asset` | Indique le profil de couleurs interne par défaut (U.S. Web Coated (SWOP) v2) automatiquement appliqué dans le cadre du &quot;comportement par défaut des couleurs&quot; lors de l’ajout de fichiers image CMJN. |
| `*`iptcExifMappingXslt`*` | `types:Asset` | L’extraction des données d’en-tête d’image IPTC et EXIF dans IPS nécessite une conversion des noms de champ internes en noms de champ définis par l’utilisateur pour l’entreprise. Détermine une table de traduction XSL (la valeur par défaut est &quot;Ne pas extraire de champs IPTC ou EXIF&quot;) pour les images téléchargées. |
| `*`xmpMappingXslt`*` | `types:Asset` | L’extraction des données d’en-tête d’image XMP dans IPS nécessite une conversion des noms de champ internes en noms de champ définis par l’utilisateur pour l’entreprise. Détermine une table de traduction XSL (la valeur par défaut est &quot;Ne pas extraire de champs XMP&quot;) pour les images téléchargées. |
| `*`diskSpaceWarningMin`*` | `xsd:int` | Quantité minimale d’espace disque disponible pour le répertoire d’images avant l’envoi d’un avertissement. |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | Détermine s’il faut envoyer des emails avant que les éléments placés dans la corbeille ne soient automatiquement supprimés. |
| `*`javascriptUploadEnabled`*` | `types:Asset` | Détermine s’il faut charger des fichiers JavaScript. Il s’agit d’un risque de sécurité potentiel. Vous devez donc utiliser cette option avec précaution. |
