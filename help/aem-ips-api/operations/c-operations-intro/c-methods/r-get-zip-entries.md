---
description: Renvoie les données d’un fichier ZIP.
solution: Experience Manager
title: getZipEntries
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: eb052685-b750-4a12-b00e-28e676340e98
TQID: 'https://experienceleague.adobe.com/-fb25TjtmLMUiZe8gRLz7QmtajqVKASUwwc6TQfjN48'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 20%

---

# getZipEntries{#getzipentries}

Renvoie les données d’un fichier ZIP.

Syntaxe

## Types d’utilisateurs autorisés {#section-33a3f03ba8a14086922397619ce12ab8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-aa3f498fe76d4a5f99c42d64520fadce}

**Input (getZipEntriesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société qui contient le fichier Zip. |
| assetHandle | `xsd:string` | Oui | Gérer vers le fichier Zip. |

**Output (getZipEntriesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| zipArray | `types:ZipEntryArray` | Oui | Tableau d’entrées dans un fichier Zip. |

## Exemples {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

Cet exemple de code renvoie des informations sur le fichier Zip, y compris sa taille compressée et non compressée.

**Requête**

```java
<getZipEntriesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|94223|27|30602</assetHandle>
</getZipEntriesParam>
```

**Réponse**

```java
<getZipEntriesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zipArray
      <items>
         <name>Checklist_Images/.DS_Store</name>
         <isDirectory>false</isDirectory>
         <lastModified>2007-05-09T15:41:52.000-07:00</lastModified>
         <compressedSize>503</compressedSize>
         <uncompressedSize>6148</uncompressedSize>
      </items>
   ...
   </zipArray>
</getZipEntriesReturn>
```

