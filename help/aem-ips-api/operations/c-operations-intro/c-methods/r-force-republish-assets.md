---
description: Réinitialise l’état de publication d’un ou de plusieurs fichiers afin de forcer la publication du fichier dans la tâche de publication suivante.
seo-description: Réinitialise l’état de publication d’un ou de plusieurs fichiers afin de forcer la publication du fichier dans la tâche de publication suivante.
seo-title: forceRepublishAssets
solution: Experience Manager
title: forceRepublishAssets
topic: Scene7 Image Production System API
uuid: fd1f4ece-075c-40e3-868a-f27b9a4c3374
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# forceRepublishAssets{#forcerepublishassets}

Réinitialise l’état de publication d’un ou de plusieurs fichiers afin de forcer la publication du fichier dans la tâche de publication suivante.

Syntaxe

## Types d’utilisateurs autorisés {#section-3d5a3e3afea748d69845de5c8c376448}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-fd3f4dde9e984240b6f3e6d7a8db4e78}

**Entrée (forceRepublishAssetsParam)**

<table id="table_742D67AD77554904976EC4A07A0CBC64"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> sociétéHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Accédez au contenant les ressources à réinitialiser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> republishFiles</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Désigne que les fichiers de la ressource sont republiés sur les serveurs  de. La valeur par défaut est <span class="codeph"> true</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> resyncCatalog</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Indique que les métadonnées de catalogue utilisées pour servir le fichier sont synchronisées pour garantir qu’il est à jour. Ce paramètre est utilisé pour résoudre les conditions de concurrence qui peuvent survenir lors de mises à jour presque simultanées du même enregistrement. Defaults to <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:HandleArray</span> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Tableau de poignées pour les fichiers dont l’état de publication doit être réinitialisé. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (forceRepublishAssetsParam)**

<table id="table_78E74186669F477E9E2D837D58A789DC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishStateUpdateArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:PublishStateUpdateArray</span> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Tableau des mises à jour de l’état de publication. </p> </td> 
  </tr> 
 </tbody> 
</table>

