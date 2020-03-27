---
description: Paramètres de configuration spécifiques aux .
seo-description: Paramètres de configuration spécifiques aux .
seo-title: CompanySettings
solution: Experience Manager
title: CompanySettings
topic: Scene7 Image Production System API
uuid: a807d5c1-058d-4313-b4f8-6ee203284003
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CompanySettings{#companysettings}

Paramètres de configuration spécifiques aux .

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| ` *`overwriteMode`*` | `xsd:string` | Détermine si les images du dossier actif doivent être remplacées par le même nom et la même extension d’image de base. |
| ` *`keepPublishState`*` | `xsd:boolean` | Indique si une image de remplacement téléchargée dans IPS doit conserver le paramètre &quot;Prêt à publier&quot; existant ou s’il doit être conforme aux spécifications du téléchargement. |
| ` *`defaultSourceProfile`*` | `types:Asset` | Indique le de couleurs source par défaut (Coated FOGRA27 (ISO 126472:2004)) appliqué automatiquement dans le cadre du &quot;comportement par défaut des couleurs&quot; lors de l’ajout de fichiers d’image CMJN. |
| ` *`defaultDisplayProfile`*` | `types:Asset` | Indique le de couleurs interne par défaut (U.S. Web Coated (SWOP) v2) automatiquement appliqué dans le cadre du &quot;comportement par défaut des couleurs&quot; lors de l’ajout de fichiers d’image CMJN. |
| ` *`iptcExifMappingXslt`*` | `types:Asset` | Le   des données d&#39;en-tête d&#39;image IPTC et EXIF dans IPS nécessite une conversion des noms de champs internes en noms de champs définis par l&#39;utilisateur pour le. Détermine un tableau de traduction XSL (la valeur par défaut est &quot;Ne pas extraire de champs IPTC ou EXIF&quot;) pour les images téléchargées. |
| ` *`xmpMappingXslt`*` | `types:Asset` | Le   des données d’en-tête d’image XMP dans IPS nécessite une conversion des noms de champ internes en noms de champ définis par l’utilisateur pour l’. Détermine un tableau de traduction XSL (par défaut, &quot;Ne pas extraire de champs XMP&quot;) pour les images téléchargées. |
| ` *`diskSpaceWarningMin`*` | `xsd:int` | Quantité minimale d’espace disque libre du répertoire d’images avant l’envoi d’un avertissement. |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | Détermine s’il faut envoyer des courriers électroniques avant que les éléments placés dans la corbeille ne soient automatiquement supprimés. |
| ` *`javascriptUploadEnabled`*` | `types:Asset` | Détermine s’il faut télécharger des fichiers JavaScript. Il s’agit d’un risque potentiel pour la sécurité. Utilisez donc cette option avec soin. |

