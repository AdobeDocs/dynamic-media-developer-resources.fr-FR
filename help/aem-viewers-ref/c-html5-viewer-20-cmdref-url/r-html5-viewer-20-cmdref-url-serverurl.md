---
description: Paramètre commun à toutes les visionneuses.
solution: Experience Manager
title: serverUrl
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# serverUrl{#serverurl}

Paramètre commun à toutes les visionneuses.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Chemin d’accès racine relatif ou absolu de la diffusion d’images. </p> <p> Indique un chemin relatif ou absolu vers la diffusion d’images, d’où la visionneuse récupère les images. Si le chemin d’accès ne comporte pas de balise <span class="filepath"> /</span>, il est relatif à l’emplacement de la page HTML de la visionneuse. Si le chemin d’accès comporte un <span class="filepath"> /</span> de début, il spécifie un chemin absolu sur le même serveur. </p> <p> N’utilisez qu’un chemin absolu au cas où le module de partage de courrier électronique serait activé dans le lecteur. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-10ee45d637134e0fbcd943c62578cb78}

Facultatif. Pas nécessaire pour l&#39;utilisation standard de SaaS (logiciel en tant que service).

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
