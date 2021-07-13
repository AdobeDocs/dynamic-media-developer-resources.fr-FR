---
description: Paramètre commun à toutes les visionneuses.
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media Classic,Visionneuses,SDK/API
role: Developer,User
exl-id: db0ce8c4-3754-4fef-9430-44ee8e5c5e80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 5%

---

# videoServerUrl{#videoserverurl}

Paramètre commun à toutes les visionneuses.

>[!NOTE]
>
>Cette commande ne s’applique pas à la visionneuse d’images vidéo.

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Chemin d’accès racine du serveur vidéo. Si aucun domaine n’est spécifié, le domaine à partir duquel la page est diffusée est appliqué à la place. La résolution standard du chemin d’accès URI s’applique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-10ee45d637134e0fbcd943c62578cb78}

Facultatif. Non requis pour l’utilisation de logiciels standard en tant que service.

## Par défaut {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Exemple {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
