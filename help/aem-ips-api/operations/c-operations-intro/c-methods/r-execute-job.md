---
description: Exécute une tâche spécifique.
solution: Experience Manager
title: executeJob
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 4b2a2a14-d785-43bd-b1fc-2812d9f21964
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 19%

---

# executeJob{#executejob}

Exécute une tâche spécifique.

Syntaxe

## Types d’utilisateurs autorisés {#section-8199e8599ea64e7097a2acb633417b15}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-2c61b2bffcf9479a9391f2c13fdf7d53}

**Entrée (executeJobParam)**

<table id="table_FA410513908F4084A21A5F0A9431006C"> 
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
   <td colname="col4"> <p>Gestionnaire de la société à laquelle appartient la tâche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> jobHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Gestionnaire de la tâche à exécuter. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Sortie (executeJobReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-96f71aa58a954293b9a98ff96d86f232}

Cet exemple de code exécute une tâche planifiée dans IPS.

**Request**

```java
<executeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</executeJobParam>
```

**Réponse**

Aucune
