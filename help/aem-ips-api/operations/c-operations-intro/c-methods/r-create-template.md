---
description: Crée une image superposée qui peut contenir plusieurs calques de texte et d’image.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 10%

---


# createTemplate{#createtemplate}

Crée une image superposée qui peut contenir plusieurs calques de texte et d’image.

Le paramètre `urlModifier` spécifie les commandes de protocole Image Server stockées dans le catalogue Image Server appliquées avant toute commande fournie par l’utilisateur sur l’URL. Le paramètre `urlPostApplyModifier` spécifie les commandes de protocole appliquées après les commandes d&#39;URL, ce qui remplace les paramètres fournis par l&#39;utilisateur en conflit.

## Types d’utilisateur autorisés {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**Entrée (createTemplateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Société à laquelle appartient le modèle. |
| `*`folderHandle`*` | `xsd:string` | Oui | Identifiant du dossier qui représente le dossier dans lequel réside le modèle. |
| `*`name`*` | `xsd:string` | Oui | Nom du modèle. |
| `*`type`*` | `xsd:string` | Oui | Type de modèle. |
| `*`urlModificateur`*` | `xsd:string` | Oui | Spécifie les commandes Image Server stockées dans le catalogue IS qui sont appliquées avant toute commande fournie par l’utilisateur sur l’URL. |
| `*`urlPostApplyModificateur`*` | `xsd:string` | Non | Spécifie les commandes de protocole appliquées après les commandes d&#39;URL, qui remplaceront tout paramètre fourni par l&#39;utilisateur en conflit. |

**Output (createTemplateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée du modèle. |

## Exemples {#section-09adb4d2f0c944af875c4463a461f55d}

Cet exemple de code crée un modèle dans un dossier spécifié par un handle, avec le nom `APIcreateTemplate`, `urlModifier` et `urlPostApplyModifier`. La réponse renvoie le handle au modèle nouvellement créé.

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

