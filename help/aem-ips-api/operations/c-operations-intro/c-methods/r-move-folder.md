---
description: Déplacer un dossier vers un nouvel emplacement.
solution: Experience Manager
title: Déplacer le dossier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 25%

---

# Déplacer le dossier{#movefolder}

Déplacer un dossier vers un nouvel emplacement.

Syntaxe

## Types d’utilisateurs autorisés {#section-7f1979fb5e504bdea3a8df01101b50c3}

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
| CompanyHandle | `xsd:string` | Oui | Manipuler à la société. |
| poignée de dossier | `xsd:string` | Oui | Poignée de dossier. |
| destFolderHandle | `xsd:string` | Oui | Poignée vers le dossier de destination. |

**Output (moveFolderReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| poignée de dossier | `xsd:string` | Oui | Gérez le dossier déplacé. |

## Exemples {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**Demander**

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
