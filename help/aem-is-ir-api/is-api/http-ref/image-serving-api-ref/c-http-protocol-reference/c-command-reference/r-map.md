---
title: carte
description: Données de la zone cliquable. Fournit des données de zone cliquable pour ce calque. Il remplace toutes les données du mappage de catalogue pour cette couche.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
TQID: 'https://experienceleague.adobe.com/9JJUVcw5-wl0B-rP-m6DC1c1DGIqxaV2UgboocFGGV8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 224
ht-degree: 2%

---

# carte{#map}

Données de la zone cliquable. Fournit des données de zone cliquable pour ce calque. Il remplace toutes les données de catalog::Map pour cette couche.

`map=[ *`string`*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Données de la zone cliquable pour ce calque en coordonnées de calque. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>Données de zone cliquable pour ce calque dans les coordonnées d’image source. </p></td> 
 </tr> 
</table>

Une chaîne vide indique que ce calque ne doit pas fournir de zone cliquable. La chaîne doit être correctement encodée en HTTP pour éviter des problèmes d’analyse.

Tous les esperluettes (&amp;) apparaissant dans *`string`* doivent être encodés en http.

Bien que `mapA=` et `catalog::Map` spécifient les données de mappage dans les coordonnées d’image source, `map=` suppose que les coordonnées du calque sont relatives au coin supérieur gauche du rectangle du calque (après l’application des `rotate=` et `extend=`).

La zone cliquable de sortie est toujours écrêtée sur le rectangle du calque. Si l’attribut `shape` est omis ou défini sur `default`, le rectangle de calque entier est utilisé comme zone cliquable.

## Propriétés {#section-a18d9ea95c71414a905a68b8839c0843}

Attribut de calque. Lorsqu’elles sont appliquées à `layer=comp`, les données de carte spécifiées sont superposées derrière toutes les autres zones cliquables. Ignoré sauf `req=map`. Ignoré par les calques d’effet. `mapA=` est ignoré si `map=` est également spécifié.

## Par défaut {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` est utilisé si `map=` n’est pas spécifié.

## Exemple {#section-cd7691c94f984222845c86dcb0051ce8}

Définissez une zone cliquable rectangulaire pour un calque de texte simple :

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Un élément `AREA` avec des attributs (principalement) par défaut est utilisé pour insérer la zone de mappage pour l’ensemble du rectangle de calque.

## Voir aussi {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Images cliquables](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
