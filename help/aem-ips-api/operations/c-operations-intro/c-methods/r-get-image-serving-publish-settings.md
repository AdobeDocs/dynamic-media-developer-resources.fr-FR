---
description: Pour un usage interne uniquement. Les utilisateurs doivent se reporter à la section Référence du catalogue d’images - Référence d’attributs du serveur d’images.
seo-description: Pour un usage interne uniquement. Les utilisateurs doivent se reporter à la section Référence du catalogue d’images - Référence d’attributs du serveur d’images.
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
topic: Scene7 Image Production System API
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

Pour un usage interne uniquement. Les utilisateurs doivent se reporter à la section Référence du catalogue d’images - Référence d’attributs du serveur d’images.

Syntaxe

## Types d’utilisateurs autorisés {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-79f0d54acd604ad2a5c96679334f2424}

**Entrée (getImageServingPublishSettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée du avec les paramètres de publication de la diffusion d’images. |
| ` *`contextHandle`*` | `xsd:string` | Oui | Traitement du contexte de publication. |

**Sortie**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`publishSettingArray`*` | `xsd:string` | Oui | Tableau des paramètres de publication du serveur d’images. |

