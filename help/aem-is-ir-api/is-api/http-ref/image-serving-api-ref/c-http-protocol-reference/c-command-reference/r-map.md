---
description: Données de zone cliquable. Fournit des données de zone cliquable pour ce calque. Remplace toutes les données de la zone cliquable du catalogue pour ce calque.
seo-description: Données de zone cliquable. Fournit des données de zone cliquable pour ce calque. Remplace toutes les données de la zone cliquable du catalogue pour ce calque.
seo-title: carte
solution: Experience Manager
title: carte
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c1c3323-21ab-4820-bf4e-761b82ada1ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# carte{#map}

Données de zone cliquable. Fournit des données de zone cliquable pour ce calque. Remplace toutes les données du catalogue::Map pour ce calque.

`map=[ *`string`*]mapA=[ *`chaîneA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>Données de zone cliquable pour ce calque en coordonnées de calque. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> chaîneA</span></span> </p></td> 
  <td class="stentry"> <p>Données de zone cliquable pour ce calque en coordonnées d’image source. </p></td> 
 </tr> 
</table>

Une chaîne vide indique que ce calque ne doit pas fournir de zone cliquable. La chaîne doit être codée correctement en HTTP pour éviter les problèmes d’analyse.

Tous les caractères d’esperluette (&amp;) survenant dans *`string`* doivent être codés au format http.

Alors que `mapA=` et `catalog::Map` spécifiez les données de mappage dans les coordonnées de l’image source, `map=` suppose que les coordonnées du calque sont relatives au coin supérieur gauche du rectangle du calque (après `rotate=` et `extend=` avoir été appliquées).

La zone cliquable de sortie est toujours coupée dans le rectangle du calque. Si l’ `shape` attribut est omis ou défini sur `default`, le rectangle du calque entier est utilisé comme zone de zone cliquable.

## Propriétés {#section-a18d9ea95c71414a905a68b8839c0843}

Attribut de calque. Lorsqu’elles sont appliquées à `layer=comp`, les données de mappage spécifiées sont superposées derrière toutes les autres zones cliquables. Ignoré sauf `req=map`. Ignoré par les calques d’effet. `mapA=` est ignorée si `map=` est également spécifiée.

## Par défaut {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` est utilisée si `map=` n’est pas spécifié.

## Exemple {#section-cd7691c94f984222845c86dcb0051ce8}

Définissez une zone cliquable rectangulaire pour un calque de texte simple :

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Un `AREA` élément avec (principalement) des attributs par défaut est utilisé pour insérer la zone de mappage pour l’ensemble du rectangle du calque.

## Voir aussi {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Zones cliquables](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
