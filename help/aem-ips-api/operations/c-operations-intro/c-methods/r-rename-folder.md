---
description: Permet de renommer un dossier.
solution: Experience Manager
title: renommer le dossier
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 2d4f1059-8018-4efb-a1ec-8eb560b1a58f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

---

# renommer le dossier{#renamefolder}

Permet de renommer un dossier.

Syntaxe

## Types d’utilisateurs autorisés {#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et en écriture à l’actif.

## Paramètres {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**Entrée (renameFolderParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Gérez le nom de l’entreprise avec les dossiers que vous souhaitez renommer. |
| poignée de dossier | `xsd:string` | Oui | Poignée dans le dossier. |
| Nom de dossier | `xsd:string` | Oui | Nouveau nom du dossier. |

**Output (renameFolderReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| poignée de dossier | `xsd:string` | Oui | Poignée dans le dossier renommé. |

## Exemples {#section-98bdd2f88d164f488676e90aba1dc864}

Cet exemple de code renomme un dossier.

**Demander**

```java
<ns1:renameFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/PDF/</ns1:folderHandle>
   <ns1:folderName>My Newly Renamed PDF Folder</ns1:folderName>
</ns1:renameFolderParam>
```

**Réponse**

```java
<renameFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderHandle>MyCompany/My Newly Renamed PDF Folder/</folderHandle>
</renameFolderReturn>
```
