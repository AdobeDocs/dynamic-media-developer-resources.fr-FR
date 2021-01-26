---
description: Crée une copie d’un fichier d’image existant. Les commandes de protocole Image Server spécifiées sont appliquées pour générer la nouvelle copie.
seo-description: Crée une copie d’un fichier d’image existant. Les commandes de protocole Image Server spécifiées sont appliquées pour générer la nouvelle copie.
seo-title: copyImage
solution: Experience Manager
title: copyImage
topic: Dynamic Media Image Production System API
uuid: ae24f0cc-bcf0-4652-a67d-ed69f8a0da92
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 19%

---


# copyImage{#copyimage}

Crée une copie d’un fichier d’image existant. Les commandes de protocole Image Server spécifiées sont appliquées pour générer la nouvelle copie.

Syntaxe

## Types d’utilisateur autorisés {#section-c9fe7abb550e495f832234f845db7d6e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-bf36fcbfda6742f5b9c6b02ea27e5b9d}

**Entrée (copyImageParam)**

<table id="table_F6B14D4875F2424D98B8C4899B1DD867"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoire </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Poignée de la société contenant l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Poignée du fichier d’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> folderHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Identifiant du dossier dans lequel l’image doit être copiée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> name</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Nom de la nouvelle image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> urlModificateur</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (copyImageParam)**

<table id="table_5E4ED83047314DFABC1BFAAC76C0EAC3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoire </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Poignée de l’image copiée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemples {#section-c30a4017001146e7befbbfc5ffcb7593}

L’exemple de code copie une image spécifiée par société, ressource, nom d’utilisateur et nom de dossier.

**Request**

```java
<copyImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>Copy_macbookwin1</name>
   <urlModifier/>
</copyImageParam>
```

**Réponse**

```java
<copyImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|943|1|580</assetHandle>
</copyImageReturn>
```

