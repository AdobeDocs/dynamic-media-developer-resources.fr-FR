---
description: Pour un usage interne uniquement. Les utilisateurs doivent se reporter à la section Référence du catalogue d’images de la diffusion d’images - Référence d’attributs.
seo-description: Pour un usage interne uniquement. Les utilisateurs doivent se reporter à la section Référence du catalogue d’images de la diffusion d’images - Référence d’attributs.
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 12%

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

