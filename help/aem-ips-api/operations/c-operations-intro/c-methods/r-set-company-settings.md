---
description: Définit différentes valeurs de configuration spécifiques à l’entreprise.
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 11%

---

# setCompanySettings{#setcompanysettings}

Définit différentes valeurs de configuration spécifiques à l’entreprise.

Syntaxe

## Types d’utilisateurs autorisés {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-a472da6c57c74a94a179dda081004888}

**Input (setCompanySettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société. |
| overwriteMode | `xsd:string` | Non | Mode de remplacement des ressources. |
| retainPublishState | `xsd:boolean` | Non | Définissez cette variable sur `true` afin de conserver l’état de publication lorsqu’une ressource est rechargée. |
| defaultSourceProfileHandle | `xsd:string` | Non | Ressource IccProfile à utiliser comme profil de couleurs source par défaut. |
| defaultDisplayProfileHandle | `xsd:string` | Non | Ressource IccProfile à utiliser comme profil de couleurs d’affichage par défaut. |
| iptcExifMappingXsltHandle | `xsd:string` | Non | Ressource XSL utilisée pour mapper les métadonnées IPTC et EXIF aux champs de métadonnées IPS. |
| xmpMappingXsltHandle | `xsd:string` | Non | Ressource XSL utilisée pour mapper les métadonnées XMP aux champs de métadonnées IPS. |
| diskSpaceWarningMin | `xsd:int` | Non | Espace disque disponible minimum (en Ko) avant l&#39;envoi d&#39;un message d&#39;avertissement. |
| emailTrashCleanupWarning | `xsd:boolean` | Non | Définissez sur `true` pour envoyer aux administrateurs de l’entreprise une notification chaque fois que des ressources sont vidées de la corbeille. |

**Output (setCompanySettingsReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

Cet exemple de code définit la configuration d’une entreprise.

**Requête**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**Réponse**

Aucune
