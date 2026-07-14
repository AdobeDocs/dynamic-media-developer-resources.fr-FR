---
description: Paramètres de configuration spécifiques à l’entreprise.
solution: Experience Manager
title: Paramètres de l’entreprise
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
TQID: 'https://experienceleague.adobe.com/iGc-AwCFbpkATjLjvSBtx4vsP0-OUDSkH2dFHZ-j2rg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 244
ht-degree: 2%

---

# [!DNL CompanySettings]{#companysettings}

Paramètres de configuration spécifiques à l’entreprise.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| overwriteMode | `xsd:string` | Détermine s’il faut remplacer les images du dossier actif avec le même nom et la même extension d’image de base. |
| retainPublishState | `xsd:boolean` | Indique si une image de remplacement chargée dans IPS doit conserver le paramètre « Prêt pour publication » existant ou s’il doit correspondre aux paramètres spécifiés par le chargement. |
| defaultSourceProfile | `types:Asset` | Indique le profil de couleurs source par défaut (Coated FOGRA27 (ISO 126472:2004)) appliqué automatiquement dans le cadre du « Comportement des couleurs par défaut » lors de l’ajout de fichiers image CMJN. |
| defaultDisplayProfile | `types:Asset` | Indique le profil de couleurs interne par défaut (U.S. Web Coated (SWOP) v2) appliqué automatiquement dans le cadre du « Comportement des couleurs par défaut » lors de l’ajout de fichiers image CMJN. |
| iptcExifMappingXslt | `types:Asset` | L’extraction des données d’en-tête d’image IPTC et EXIF dans IPS nécessite une conversion des noms de champ internes en noms de champ définis par l’utilisateur pour la société. Détermine une table de traduction XSL (par défaut : « N’extrayez aucun champ IPTC ou EXIF ») pour les images chargées. |
| xmpMappingXslt | `types:Asset` | L’extraction des données d’en-tête d’image XMP dans IPS nécessite une conversion des noms de champ internes en noms de champ définis par l’utilisateur pour la société. Détermine une table de traduction XSL (par défaut : « Ne pas extraire de champs XMP ») pour les images chargées. |
| diskSpaceWarningMin | `xsd:int` | Quantité minimale d’espace disque disponible dans le répertoire d’images avant l’envoi d’un avertissement. |
| emailTrashCleanupWarning | `xsd:boolean` | Détermine s&#39;il faut envoyer des e-mails avant que les éléments de corbeille ne soient automatiquement supprimés. |
| javascriptUploadEnabled | `types:Asset` | Détermine s’il faut charger les fichiers JavaScript. Cette option présente un risque potentiel pour la sécurité. Utilisez-la avec précaution. |

