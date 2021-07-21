---
description: Supprime les autorisations de dossier.
solution: Experience Manager
title: removeFolderPermissions
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 10830980-d504-4610-96c9-730937453256
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 16%

---

# removeFolderPermissions{#removefolderpermissions}

Supprime les autorisations de dossier.

Syntaxe

## Types d’utilisateurs autorisés {#section-bfa745624f9b43aaba6c226ac6700fe7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-7efa68377fd846219b906d354ae64ed3}

**Entrée (removeFolderPermissionsParam)**

<table id="table_15223256C63C4F008BDB1DF6F0AFE6A8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Obligatoire </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Gestion de l’entreprise avec les dossiers avec les autorisations que vous souhaitez supprimer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Gérer au dossier. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChildren</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Lorsque <span class="codeph"> true</span> : 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">La suppression des autorisations se propage par toutes les opérations d’autorisation de dossier. </li> 
     </ul> </p> <p>Lorsque <span class="codeph"> false</span> : 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">L’opération affecte uniquement le dossier spécifié. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Sortie (removeFolderPermissionsReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-04390f0ec7cc460cb5d34d518e33e7a5}

Cet exemple de code supprime les autorisations d’un dossier et de ses sous-dossiers. Définissez `updateChildren` sur `false` si vous devez supprimer des autorisations du dossier parent uniquement.

**Request**

```java
<removeFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <updateChildren>true</updateChildren>
</removeFolderPermissionsParam>
```

**Réponse**

Aucune
