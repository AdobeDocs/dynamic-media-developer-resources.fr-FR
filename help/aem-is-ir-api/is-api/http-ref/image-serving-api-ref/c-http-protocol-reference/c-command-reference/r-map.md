---
description: Données de zone cliquable. Fournit des données de zone cliquable pour ce calque. Remplace toutes les données de la zone cliquable du catalogue pour ce calque.
solution: Experience Manager
title: carte
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---


# carte{#map}

Données de zone cliquable. Fournit des données de zone cliquable pour ce calque. Remplace toutes les données de catalog::Map pour ce calque.

`map=[ *``*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Données de zone cliquable pour ce calque en coordonnées de calque. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>Données de zone cliquable pour ce calque en coordonnées d’image source. </p></td> 
 </tr> 
</table>

Une chaîne vide indique que ce calque ne doit pas fournir de zone cliquable. La chaîne doit être codée correctement en HTTP pour éviter les problèmes d’analyse.

Tous les caractères d’esperluette (&amp;) survenant dans *`string`* doivent être codés au format http.

Bien que `mapA=` et `catalog::Map` spécifient les données de mappage dans les coordonnées de l’image source, `map=` suppose que les coordonnées de calque sont relatives au coin supérieur, à gauche du rectangle du calque (après l’application des paramètres `rotate=` et `extend=`).

La zone cliquable de sortie est toujours coupée dans le rectangle du calque. Si l’attribut `shape` est omis ou défini sur `default`, l’ensemble du rectangle de calque est utilisé comme zone de zone cliquable.

## Propriétés {#section-a18d9ea95c71414a905a68b8839c0843}

Attribut de couche. Lorsqu’elle est appliquée à `layer=comp`, les données de mappage spécifiées sont superposées derrière toutes les autres zones cliquables. Ignoré sauf si `req=map`. Ignoré par les calques d’effet. `mapA=` est ignoré si  `map=` est également spécifié.

## Par défaut {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` est utilisé si  `map=` n’est pas spécifié.

## Exemple {#section-cd7691c94f984222845c86dcb0051ce8}

Définissez une zone cliquable rectangulaire pour un calque de texte simple :

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Un élément `AREA` avec (principalement) des attributs par défaut est utilisé pour insérer la zone de mappage pour l’ensemble du rectangle de calque.

## Voir aussi {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Zones cliquables](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab),  [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
