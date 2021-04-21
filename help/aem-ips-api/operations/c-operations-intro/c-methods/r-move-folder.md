---
description: Déplacez un dossier vers un nouvel emplacement.
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '67'
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
| `*`companyHandle`*` | `xsd:string` | Oui | Pose la société. |
| `*`folderHandle`*` | `xsd:string` | Oui | Poignée de dossier. |
| `*`destFolderHandle`*` | `xsd:string` | Oui | Accédez au dossier de destination. |

**Output (moveFolderReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Oui | Pointez sur le dossier déplacé. |

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

