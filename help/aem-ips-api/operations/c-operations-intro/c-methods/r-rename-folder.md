---
description: Renomme un dossier.
solution: Experience Manager
title: renameFolder
feature: Dynamic Media Classic,SDK/API,Gestion des ressources
role: Developer,Admin
exl-id: 2d4f1059-8018-4efb-a1ec-8eb560b1a58f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 20%

---

# renameFolder{#renamefolder}

Renomme un dossier.

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
>L’utilisateur doit disposer d’un accès en lecture et en écriture à la ressource.

## Paramètres {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**Entrée (renameFolderParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Gérer la société avec les dossiers que vous souhaitez renommer. |
| `*`folderHandle`*` | `xsd:string` | Oui | Gérer au dossier. |
| `*`folderName`*` | `xsd:string` | Oui | Nouveau nom du dossier. |

**Sortie (renameFolderReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Oui | Gérer au dossier renommé. |

## Exemples {#section-98bdd2f88d164f488676e90aba1dc864}

Cet exemple de code renomme un dossier.

**Request**

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
