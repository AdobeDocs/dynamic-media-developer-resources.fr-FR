---
title: carte
description: Données de zone cliquable. Fournit des données de zone cliquable pour cette couche. Remplace toutes les données de la carte du catalogue pour cette couche.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# carte{#map}

Données de zone cliquable. Fournit des données de zone cliquable pour cette couche. Remplace toutes les données de catalog ::Map pour cette couche.

`map=[ *`chaîne`*]mapA=[ *`string A`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> corde</span></span> </p></td> 
  <td class="stentry"> <p>Données de zone cliquable pour cette couche en coordonnées de calque. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> chaîneA</span></span> </p></td> 
  <td class="stentry"> <p>Données de zone cliquable pour cette couche en coordonnées d’image source. </p></td> 
 </tr> 
</table>

Une chaîne vide indique que ce calque ne doit pas fournir de zone cliquable. La chaîne doit être correctement codée en HTTP pour éviter les problèmes d’analyse.

Toutes les esperluettes (&amp;) apparaissant dans *`string`* doivent être codées en HTTP.

Bien que `mapA=` et `catalog::Map` spécifier les données de carte dans les coordonnées de l’image source, `map=` suppose les coordonnées de couche par rapport au coin supérieur gauche du rectangle de couche (après `rotate=` et `extend=` ont été appliqués).

La zone cliquable de sortie est toujours écrêtée sur le rectangle du calque. Si l’attribut `shape` est omis ou défini sur `default`, le rectangle de calque entier est utilisé comme zone de zone cliquable.

## Propriétés {#section-a18d9ea95c71414a905a68b8839c0843}

Attribut de calque. Lorsqu’elles sont appliquées à `layer=comp`, les données de carte spécifiées sont superposées derrière toutes les autres zones cliquables. Ignoré sauf si `req=map`. Ignoré par les calques d’effets. `mapA=` est ignorée si `map=` est également spécifiée.

## Par défaut {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` est utilisé si n’est `map=` pas spécifié.

## Exemple {#section-cd7691c94f984222845c86dcb0051ce8}

Définissez une zone cliquable rectangulaire pour un calque de texte simple :

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Un `AREA` élément avec (principalement) des attributs par défaut est utilisé pour insérer la zone de carte pour l’ensemble du rectangle de couche.

## Voir aussi {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Images cliquables](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
