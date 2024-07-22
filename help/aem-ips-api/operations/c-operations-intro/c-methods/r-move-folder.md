---
description: Déplacez un dossier vers un nouvel emplacement.
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 25%

---

# moveFolder{#movefolder}

Déplacez un dossier vers un nouvel emplacement.

Syntaxe

## Types d’utilisateurs autorisés {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-473c2e68bcc14a9ea2593bee26e679dd}

**Input (moveFolderParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Traitez la société. |
| folderHandle | `xsd:string` | Oui | Poignée de dossier. |
| destFolderHandle | `xsd:string` | Oui | Gérer vers le dossier de destination. |

**Sortie (moveFolderReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| folderHandle | `xsd:string` | Oui | Gérer au dossier déplacé. |

## Exemples {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**Requête**

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
