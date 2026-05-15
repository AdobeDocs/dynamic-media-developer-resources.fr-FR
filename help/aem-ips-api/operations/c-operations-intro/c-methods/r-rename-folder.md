---
description: Renomme un dossier.
solution: Experience Manager
title: renameFolder
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 2d4f1059-8018-4efb-a1ec-8eb560b1a58f
TQID: 'https://experienceleague.adobe.com/8joB9mgnIpAn2IuXk97bztqa-IbskzuDcWUoMtJ5Sjk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 75
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
>L’utilisateur doit disposer d’un accès en lecture et écriture à la ressource.

## Paramètres {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**Input (renameFolderParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gérer vers la société avec les dossiers à renommer. |
| folderHandle | `xsd:string` | Oui | Gérer vers le dossier . |
| folderName | `xsd:string` | Oui | Nom du nouveau dossier. |

**Output (renameFolderReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| folderHandle | `xsd:string` | Oui | Gérer vers le dossier renommé. |

## Exemples {#section-98bdd2f88d164f488676e90aba1dc864}

Cet exemple de code renomme un dossier.

**Requête**

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
