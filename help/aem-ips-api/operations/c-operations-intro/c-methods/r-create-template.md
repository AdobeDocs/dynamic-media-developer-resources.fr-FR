---
description: Crée une image superposée pouvant contenir plusieurs calques de texte et d’image.
seo-description: Crée une image superposée pouvant contenir plusieurs calques de texte et d’image.
seo-title: createTemplate
solution: Experience Manager
title: createTemplate
topic: Scene7 Image Production System API
uuid: c54bd47c-13e1-4b0d-a24c-9829b0a6d5bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createTemplate{#createtemplate}

Crée une image superposée pouvant contenir plusieurs calques de texte et d’image.

Le `urlModifier` paramètre spécifie les commandes de protocole Image Server stockées dans le catalogue Image Server appliquées avant les commandes fournies par l’utilisateur sur l’URL. Le `urlPostApplyModifier` paramètre spécifie les commandes de protocole appliquées après les commandes d’URL, ce qui remplace les paramètres fournis par l’utilisateur en conflit.

## Types d’utilisateurs autorisés {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**Input (createTemplateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | auquel appartient le modèle. |
| ` *`folderHandle`*` | `xsd:string` | Oui | Identifiant du dossier qui représente le dossier dans lequel réside le modèle. |
| ` *`nom`*` | `xsd:string` | Oui | Nom du modèle. |
| ` *`type`*` | `xsd:string` | Oui | Type de modèle. |
| ` *`urlModificateur`*` | `xsd:string` | Oui | Spécifie les commandes Image Server stockées dans le catalogue IS qui sont appliquées avant les commandes fournies par l’utilisateur sur l’URL. |
| ` *`urlPostApplyModificateur`*` | `xsd:string` | Non | Spécifie les commandes de protocole appliquées après les commandes d’URL, qui remplaceront les paramètres fournis par l’utilisateur en conflit. |

**Output (createTemplateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Oui | Poignée du modèle. |

## Exemples {#section-09adb4d2f0c944af875c4463a461f55d}

Cet exemple de code crée un modèle dans un dossier spécifié par une poignée, avec le nom `APIcreateTemplate`, un `urlModifier`et un `urlPostApplyModifier`. La réponse renvoie le pseudo au modèle nouvellement créé.

**Request**

```java
<createTemplateParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>APIcreateTemplate</name>
   <type>Template</type>
   <urlModifier>url=Modifier</urlModifier>
   <urlPostApplyModifier>urlPostApply=Modifier</urlPostApplyModifier>
</createTemplateParam>
```

**Réponse**

```java
<createTemplateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|153393|2|2061</assetHandle>
</createTemplateReturn>
```

