---
description: Paramètre commun à toutes les visionneuses.
solution: Experience Manager
title: config
feature: Dynamic Media Classic,Visionneuses,SDK/API
role: Developer,User
exl-id: 503a1fc6-7a6b-4f55-bad1-11f22435276f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 4%

---

# config{#config}

Paramètre commun à toutes les visionneuses.

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId  </span> </span> </p> </td> 
   <td colname="col2"> <p>Catalogue/ID pour la configuration de la visionneuse. </p> <p> Spécifie une entrée de catalogue d’images contenant les propriétés de configuration de la visionneuse dans <span class="codeph"> catalog::UserData </span>. Lorsque cette commande est présente, la visionneuse envoie une commande <span class="codeph"> req=userdata </span> pour <span class="codeph"> configId </span> au serveur et extrait les propriétés de la réponse. Les propriétés sont utilisées pour initialiser la visionneuse. Si la chaîne URL spécifie les mêmes propriétés, elles remplacent les valeurs de <span class="codeph"> catalog::UserData </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Toutes les commandes de visionneuse qui peuvent être spécifiées dans `catalog::UserData` s’attendent à ce que `asset`, `serverUrl`, `contentUrl`, `searchServerUrl` et `config` elles-mêmes.

## Propriétés {#section-10ee45d637134e0fbcd943c62578cb78}

Facultatif.

## Par défaut {#section-d411e450028c460392cb8508f8ccc5d9}

Aucune

## Exemple 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Un catalogue d’images nommé 2020 contient l’entrée `preset-oct`. Le champ `catalog::UserData` de cette entrée de catalogue contient les données suivantes :

```
style=customStyle.css
```

Chargez la visionneuse à l’aide de la commande suivante :

```
config=2020/preset-oct
```

Cela équivaut aux commandes suivantes spécifiées explicitement dans l’URL :

```
style=customStyle.css
```

## Exemple 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

Un catalogue d’images nommé 2019 contient l’entrée `spin-oct`. Le champ `catalog::UserData` de cette entrée de catalogue contient les données suivantes :

```
zoomStep=3 
maxZoom=200
```

Chargez la visionneuse à l’aide de la commande suivante :

```
config=2019/spin-oct
```

Cela équivaut aux commandes suivantes spécifiées explicitement dans l’URL :

```
zoomStep=3&maxZoom=200
```

## Exemple 3 {#section-2b3a42c3926e4eb19fa14434def9195f}

Un paramètre prédéfini de visionneuse nommé `Shoppable_Banner` comprend les données suivantes :

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

Chargez la visionneuse à l’aide de la commande suivante :

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

Cela équivaut aux commandes suivantes spécifiées explicitement dans l’URL :

`style=etc/dam/presets/css/html5_interactiveimage.css`

## Exemple 4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

Un paramètre prédéfini de visionneuse nommé `Shoppable_Video_Dark` contient les données suivantes :

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

Chargez la visionneuse à l’aide de la commande suivante :

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

Cela équivaut aux commandes suivantes spécifiées explicitement dans l’URL :

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## Exemple 5 {#section-19b988551d1d492a9079948e0b04b38f}

Un paramètre prédéfini de visionneuse nommé `Carousel_Dotted_light` contient les données suivantes :

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

Chargez la visionneuse à l’aide de la commande suivante :

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

Cela équivaut aux commandes suivantes spécifiées explicitement dans l’URL :

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```
