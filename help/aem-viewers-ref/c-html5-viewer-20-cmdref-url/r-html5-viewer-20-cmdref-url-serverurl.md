---
description: Paramètre commun à toutes les visionneuses.
solution: Experience Manager
title: serverUrl
feature: Dynamic Media Classic,Visionneuses,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---

# serverUrl{#serverurl}

Paramètre commun à toutes les visionneuses.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Chemin racine relatif ou absolu de la diffusion d’images. </p> <p> Indique un chemin relatif ou absolu vers le serveur d’images, à partir duquel la visionneuse récupère les images. Si le chemin d’accès ne comporte pas de <span class="filepath"> /</span> de début, il est relatif à l’emplacement de la page HTML de la visionneuse. Si le chemin comporte un <span class="filepath"> /</span> de début, il spécifie un chemin absolu sur le même serveur. </p> <p> Utilisez uniquement un chemin absolu si le module de partage de courrier électronique est activé dans la visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-10ee45d637134e0fbcd943c62578cb78}

Facultatif. Inutile pour l’utilisation standard de SaaS (logiciel en tant que service).

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
