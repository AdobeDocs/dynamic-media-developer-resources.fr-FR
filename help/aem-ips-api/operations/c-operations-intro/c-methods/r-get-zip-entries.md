---
description: Renvoie les données du fichier Zip.
solution: Experience Manager
title: getZipEntries
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 20%

---


# getZipEntries{#getzipentries}

Renvoie les données du fichier Zip.

Syntaxe

## Types d’utilisateur autorisés {#section-33a3f03ba8a14086922397619ce12ab8}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Identifiant de la société contenant le fichier Zip. |
| `*`assetHandle`*` | `xsd:string` | Oui | Traitez le fichier Zip. |

**Output (getZipEntriesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`zipArray`*` | `types:ZipEntryArray` | Oui | Tableau des entrées dans un fichier Zip. |

## Exemples {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

Cet exemple de code renvoie des informations sur le fichier Zip, y compris la taille compressée et non compressée.

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

