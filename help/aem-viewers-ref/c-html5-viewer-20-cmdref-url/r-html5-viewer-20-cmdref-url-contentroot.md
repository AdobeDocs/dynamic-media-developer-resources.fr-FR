---
description: Paramètre commun à toutes les visionneuses.
seo-description: Paramètre commun à toutes les visionneuses.
seo-title: contentUrl
solution: Experience Manager
title: contentUrl
topic: Dynamic media
uuid: 85b00c4e-b382-4970-b780-e4ef59108cb7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# contentUrl{#contenturl}

Paramètre commun à toutes les visionneuses.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span></span> </p> </td> 
   <td colname="col2"> <p>Indique le chemin de base vers les fichiers CSS personnalisés, tout contenu de sous-titrage ou de navigation. </p> <p>Si le chemin d’accès n’a pas de caractère <span class="filepath"> /</span>de début, il dépend de l’emplacement de la page HTML de la visionneuse. Si le chemin d’accès comporte un / <span class="filepath"></span>de début, il spécifie un chemin absolu sur le même serveur. </p> <p> N’affecte pas le chargement du fichier CSS par défaut lorsque vous ne spécifiez pas de commande de style. </p> </td> 
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

