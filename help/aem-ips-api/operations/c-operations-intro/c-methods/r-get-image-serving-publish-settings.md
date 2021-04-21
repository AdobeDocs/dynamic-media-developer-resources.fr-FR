---
description: Pour un usage interne uniquement. Les utilisateurs doivent se reporter à la section Référence du catalogue d’images de la diffusion d’images - Référence d’attributs.
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 14%

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

