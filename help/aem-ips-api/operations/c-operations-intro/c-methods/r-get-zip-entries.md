---
description: Renvoie les données du fichier zip.
solution: Experience Manager
title: getZipEntries
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: eb052685-b750-4a12-b00e-28e676340e98
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 21%

---

# getZipEntries{#getzipentries}

Renvoie les données du fichier zip.

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

**Entrée (getZipEntriesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Gestionnaire de la société qui contient le fichier ZIP. |
| `*`assetHandle`*` | `xsd:string` | Oui | Gérez le fichier zip. |

**Sortie (getZipEntriesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`zipArray`*` | `types:ZipEntryArray` | Oui | Tableau d’entrées dans un fichier Zip. |

## Exemples {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

Cet exemple de code renvoie des informations sur le fichier zip, y compris la taille compressée et non compressée.

**Request**

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
