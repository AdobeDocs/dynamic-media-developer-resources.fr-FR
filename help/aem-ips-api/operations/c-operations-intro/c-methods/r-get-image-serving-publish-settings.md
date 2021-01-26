---
description: Pour un usage interne uniquement. Les utilisateurs doivent se reporter à la section Référence du catalogue d’images de la diffusion d’images - Référence d’attributs.
seo-description: Pour un usage interne uniquement. Les utilisateurs doivent se reporter à la section Référence du catalogue d’images de la diffusion d’images - Référence d’attributs.
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
topic: Dynamic Media Image Production System API
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 13%

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

Pour un usage interne uniquement. Les utilisateurs doivent se reporter à la section Référence du catalogue d’images de la diffusion d’images - Référence d’attributs.

Syntaxe

## Types d’utilisateur autorisés {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-79f0d54acd604ad2a5c96679334f2424}

**Entrée (getImageServingPublishSettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée vers la société avec les paramètres de publication de la diffusion d’images. |
| `*`contextHandle`*` | `xsd:string` | Oui | Traitement du contexte de publication. |

**Sortie**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | Oui | Tableau des paramètres de publication du serveur d’images. |

