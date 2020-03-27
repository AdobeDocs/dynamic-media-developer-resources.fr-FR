---
description: Paramètre commun à toutes les visionneuses.
seo-description: Paramètre commun à toutes les visionneuses.
seo-title: serverUrl
solution: Experience Manager
title: serverUrl
topic: Dynamic media
uuid: a079a223-7478-4b6a-bc99-284e3366fb30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# serverUrl{#serverurl}

Paramètre commun à toutes les visionneuses.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span></span> </p> </td> 
   <td colname="col2"> <p>Chemin racine relatif ou absolu du serveur d’images. </p> <p> Indique un chemin relatif ou absolu vers Image Serving, à partir duquel le lecteur récupère les images. Si le chemin d’accès n’a pas de caractère <span class="filepath"> /</span>de début, il dépend de l’emplacement de la page HTML de la visionneuse. Si le chemin d’accès comporte un / <span class="filepath"></span>de début, il spécifie un chemin absolu sur le même serveur. </p> <p> N’utilisez qu’un chemin absolu au cas où le module Partage de courrier électronique serait activé dans le lecteur. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-10ee45d637134e0fbcd943c62578cb78}

Facultatif. Pas nécessaire pour l’utilisation standard de SaaS (logiciel en tant que service).

## Par défaut {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## Exemples {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```

