---
description: Paramètre commun à toutes les visionneuses.
solution: Experience Manager
title: contentUrl
feature: Dynamic Media Classic, Visionneuses, SDK/API
role: Développeur, Professionnel
exl-id: cab3c3fe-1a64-4a50-8559-57cadb31f689
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---

# contentUrl{#contenturl}

Paramètre commun à toutes les visionneuses.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Indique le chemin de base vers les fichiers CSS personnalisés, tout contenu de sous-titrage ou de navigation. </p> <p>Si le chemin d’accès ne comporte pas de balise <span class="filepath"> /</span>, il est relatif à l’emplacement de la page HTML de la visionneuse. Si le chemin d’accès comporte un <span class="filepath"> /</span> de début, il spécifie un chemin absolu sur le même serveur. </p> <p> N’affecte pas le chargement du fichier CSS par défaut lorsque vous ne spécifiez pas de commande de style. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-10ee45d637134e0fbcd943c62578cb78}

Facultatif.

## Par défaut {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Exemples {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
contentUrl=/skins/
```

```
contentUrl=http://aodmarketingna.assetsadobe.com/
```

```
contentUrl=https://demos-pub.assetsadobe.com/
```
