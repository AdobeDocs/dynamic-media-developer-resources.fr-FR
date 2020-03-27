---
description: Définit différentes valeurs de configuration spécifiques à un.
seo-description: Définit différentes valeurs de configuration spécifiques à un.
seo-title: setCompanySettings
solution: Experience Manager
title: setCompanySettings
topic: Scene7 Image Production System API
uuid: 5908082f-6743-4444-ba73-757ad4664890
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setCompanySettings{#setcompanysettings}

Définit différentes valeurs de configuration spécifiques à un.

Syntaxe

## Types d’utilisateurs autorisés {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-a472da6c57c74a94a179dda081004888}

**Entrée (setCompanySettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui |  poignée. |
| ` *`overwriteMode`*` | `xsd:string` | Non | Mode de remplacement des ressources. |
| ` *`keepPublishState`*` | `xsd:boolean` | Non | Définissez cette option sur `true` pour conserver l’état de publication lorsqu’un fichier est rechargé. |
| ` *`defaultSourceProfileHandle`*` | `xsd:string` | Non | Fichier IccProfile à utiliser comme de couleurs source par défaut. |
| ` *`defaultDisplayProfileHandle`*` | `xsd:string` | Non | Fichier IccProfile à utiliser comme de couleurs d’affichage par défaut. |
| ` *`iptcExifMappingXsltHandle`*` | `xsd:string` | Non | Ressource XSL utilisée pour mapper les métadonnées IPTC et EXIF aux champs de métadonnées IPS. |
| ` *`xmpMappingXsltHandle`*` | `xsd:string` | Non | Fichier XSL utilisé pour mapper les métadonnées XMP aux champs de métadonnées IPS. |
| ` *`diskSpaceWarningMin`*` | `xsd:int` | Non | Espace disque disponible minimum (en Ko) avant l’envoi d’un message d’avertissement. |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | Non | Permet `true` d’envoyer une notification aux administrateurs  chaque fois que des ressources sont vidées de la corbeille. |

**Output (setCompanySettingsReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

Cet exemple de code définit une configuration .

**Request**

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
