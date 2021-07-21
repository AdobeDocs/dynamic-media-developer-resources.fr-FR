---
description: Crée une image superposée pouvant comporter plusieurs calques de texte et d’image.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 10%

---

# createTemplate{#createtemplate}

Crée une image superposée pouvant comporter plusieurs calques de texte et d’image.

Le paramètre `urlModifier` spécifie les commandes de protocole Image Server stockées dans le catalogue Image Server appliquées avant toute commande fournie par l’utilisateur sur l’URL. Le paramètre `urlPostApplyModifier` spécifie les commandes de protocole appliquées après toutes les commandes d’URL, qui remplaceront les paramètres fournis par l’utilisateur en conflit.

## Types d’utilisateurs autorisés {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**Entrée (createTemplateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Société à laquelle le modèle appartient. |
| `*`folderHandle`*` | `xsd:string` | Oui | La gestion des dossiers qui représente le dossier dans lequel réside le modèle. |
| `*`name`*` | `xsd:string` | Oui | Nom du modèle. |
| `*`type`*` | `xsd:string` | Oui | Type de modèle. |
| `*`urlModifier`*` | `xsd:string` | Oui | Spécifie les commandes du serveur d’images stockées dans le catalogue IS qui sont appliquées avant toute commande fournie par l’utilisateur sur l’URL. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Non | Spécifie les commandes de protocole appliquées après toute commande d’URL, qui remplacera les paramètres fournis par l’utilisateur en conflit. |

**Output (createTemplateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Oui | Gestionnaire du modèle. |

## Exemples {#section-09adb4d2f0c944af875c4463a461f55d}

Cet exemple de code crée un modèle dans un dossier spécifié par une poignée, avec le nom `APIcreateTemplate`, `urlModifier` et une balise `urlPostApplyModifier`. La réponse renvoie le gestionnaire au modèle nouvellement créé.

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
