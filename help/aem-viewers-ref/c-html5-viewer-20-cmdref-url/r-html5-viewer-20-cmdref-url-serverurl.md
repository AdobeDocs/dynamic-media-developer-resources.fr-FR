---
title: serverUrl
description: Paramètre commun à tous les observateurs.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
TQID: 'https://experienceleague.adobe.com/SbAeHSjxnw-69wsu92UeoEeGLlk3Ykpechs65I-k5EY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 3%

---

# serverUrl{#serverurl}

Paramètre commun à tous les observateurs.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Chemin d’accès racine relatif ou absolu de la diffusion d’images. </p> <p> Indique un chemin d’accès relatif ou absolu à la diffusion d’images, à partir duquel la visionneuse récupère les images. Si le chemin d’accès ne comporte pas de <span class="filepath"> de début /</span>, il est relatif à l’emplacement de la page HTML de la visionneuse. Si le chemin comporte un <span class="filepath"> initial /</span>, il spécifie un chemin absolu sur le même serveur. </p> <p> N’utilisez qu’un chemin absolu si le module de partage d’e-mail est activé dans la visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-10ee45d637134e0fbcd943c62578cb78}

Facultatif. Non nécessaire pour une utilisation standard du SaaS (logiciel en tant que service).

## Par défaut {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## Exemples {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

<!--

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```

-->
