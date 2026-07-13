---
description: Pour usage interne uniquement. Les utilisateurs doivent se reporter à la section Référence du catalogue d’images de la diffusion d’images - Référence d’attribut .
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
TQID: 'https://experienceleague.adobe.com/-VBxIs4EWFDesksSnU-DpN2pg-LJUN60OPhqjQVqAr8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 80
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

