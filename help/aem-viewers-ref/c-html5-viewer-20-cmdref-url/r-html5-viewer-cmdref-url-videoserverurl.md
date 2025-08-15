---
title: videoServerUrl
description: Paramètre commun à tous les observateurs.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db0ce8c4-3754-4fef-9430-44ee8e5c5e80
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 3%

---

# videoServerUrl{#videoserverurl}

Paramètre commun à tous les observateurs.

>[!NOTE]
>
>Cette commande ne concerne pas la visionneuse d’images vidéo.

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Chemin d’accès racine du serveur vidéo. Si aucun domaine n’est spécifié, le domaine à partir duquel la page est diffusée est appliqué à la place. La résolution de chemin d’URI standard s’applique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-10ee45d637134e0fbcd943c62578cb78}

Facultatif. Non nécessaire pour l’utilisation de logiciels en tant que services standard.

## Par défaut {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Exemple {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
