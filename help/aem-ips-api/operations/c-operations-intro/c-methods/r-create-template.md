---
description: Crée une image superposée pouvant comporter plusieurs calques de texte et d’image.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
TQID: 'https://experienceleague.adobe.com/T9x2yuGOkwJ5xp6CVyREMySIy7HYL58jYI3-J2E2K6g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 9%

---

# createTemplate{#createtemplate}

Crée une image superposée pouvant comporter plusieurs calques de texte et d’image.

Le paramètre `urlModifier` spécifie les commandes de protocole du serveur d’images stockées dans le catalogue du serveur d’images appliquées avant toute commande fournie par l’utilisateur sur l’URL. Le paramètre `urlPostApplyModifier` spécifie les commandes de protocole appliquées après toute commande d’URL, ce qui remplace tout paramètre en conflit fourni par l’utilisateur.

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
| companyHandle | `xsd:string` | Oui | Société à laquelle le modèle appartient. |
| folderHandle | `xsd:string` | Oui | Poignée de dossier représentant le dossier dans lequel réside le modèle. |
| nom | `xsd:string` | Oui | Nom du modèle. |
| type | `xsd:string` | Oui | Type de modèle. |
| urlModifier | `xsd:string` | Oui | Spécifie les commandes du serveur d’images stockées dans le catalogue IS qui sont appliquées avant toute commande fournie par l’utilisateur sur l’URL. |
| urlPostApplyModifier | `xsd:string` | Non | Spécifie les commandes de protocole appliquées après les commandes d&#39;URL, ce qui remplace les paramètres en conflit fournis par l&#39;utilisateur. |

**Output (createTemplateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| assetHandle | `xsd:string` | Oui | Poignée du modèle. |

## Exemples {#section-09adb4d2f0c944af875c4463a461f55d}

Cet exemple de code crée un modèle dans un dossier spécifié par un objet Handle, avec un nom `APIcreateTemplate`, un `urlModifier` et un `urlPostApplyModifier`. La réponse renvoie la poignée au modèle nouvellement créé.

**Requête**

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
