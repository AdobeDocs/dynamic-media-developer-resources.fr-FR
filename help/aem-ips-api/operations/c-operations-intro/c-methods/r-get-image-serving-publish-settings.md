---
description: Pour usage interne uniquement. Les utilisateurs doivent se reporter à la section Référence du catalogue d’images de la diffusion d’images - Référence d’attribut .
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 16%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

Pour usage interne uniquement. Les utilisateurs doivent se reporter à la section Référence du catalogue d’images de la diffusion d’images - Référence d’attribut .

Syntaxe

## Types d’utilisateurs autorisés {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-79f0d54acd604ad2a5c96679334f2424}

**Input (getImageServingPublishSettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | La poignée de la société avec les paramètres de publication du service d’images. |
| contextHandle | `xsd:string` | Oui | Gérer vers le contexte de publication. |

**Output**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| publishSettingArray | `xsd:string` | Oui | Tableau des paramètres de publication du serveur d’images. |
