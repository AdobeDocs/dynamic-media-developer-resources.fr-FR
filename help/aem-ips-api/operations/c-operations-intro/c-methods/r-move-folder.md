---
description: Déplacez un dossier vers un nouvel emplacement.
seo-description: Déplacez un dossier vers un nouvel emplacement.
seo-title: moveFolder
solution: Experience Manager
title: moveFolder
topic: Scene7 Image Production System API
uuid: 424858c3-5796-4ae9-b5ad-fd50ddbee702
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 25%

---


# moveFolder{#movefolder}

Déplacez un dossier vers un nouvel emplacement.

Syntaxe

## Types d’utilisateur autorisés {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-473c2e68bcc14a9ea2593bee26e679dd}

**Entrée (moveFolderParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Pose la société. |
| ` *`folderHandle`*` | `xsd:string` | Oui | Poignée de dossier. |
| ` *`destFolderHandle`*` | `xsd:string` | Oui | Accédez au dossier de destination. |

**Output (moveFolderReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Oui | Pointez sur le dossier déplacé. |

## Exemples {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**Request**

```java
<moveFolderParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <companyHandle>c|101</companyHandle>
   <folderHandle>f|test/MoveTest/</folderHandle>
   <destFolderHandle>f|DevanCo/DestFolder/</destFolderHandle>
</moveFolderParam>
```

**Réponse**

```java
<moveFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <folderHandle>f|test/DestFolder/MoveTest/</folderHandle>
</moveFolderReturn>
```

