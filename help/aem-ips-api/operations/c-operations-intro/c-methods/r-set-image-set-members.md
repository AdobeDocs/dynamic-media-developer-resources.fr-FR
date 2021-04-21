---
description: Définit la liste des fichiers associés à une visionneuse d’images.
solution: Experience Manager
title: setImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 12%

---


# setImageSetMembers{#setimagesetmembers}

Définit la liste des fichiers associés à une visionneuse d’images.

Cette opération ignore le paramètre `pageReset` pour `ImageSets` et `SpinSets` et force la valeur sur true.

## Types d’utilisateur autorisés {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et en écriture au fichier de visionneuse d’images et d’un accès en lecture à chaque fichier membre.

## Paramètres {#section-2f46efcd24c648aeacba738509426e46}

**Entrée (setImageSetMembersParam)**

<table id="table_0CBBB65BCEFD4125A4069A080DFC873A"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Poignée de société. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Poignée de visionneuse d’images. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> MemberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Tableau des membres de fichier qui appartiennent à la visionneuse d’images. </td> 
  </tr> 
 </tbody> 
</table>

**Output (setImageSetMembersReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-7b87219034464aa98524178ccee27738}

Cet exemple de code utilise un tableau de membres pour définir les membres d’une visionneuse d’images.

**Request**

```java
<setImageSetMembersParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>34205|22|929</assetHandle>
   <memberArray>
      <items>
         <assetHandle>24266|1|17062</assetHandle>
         <pageReset>true</pageReset>
      </items>
   </memberArray>
</setImageSetMembersParam>
```

**Réponse**

Aucune
