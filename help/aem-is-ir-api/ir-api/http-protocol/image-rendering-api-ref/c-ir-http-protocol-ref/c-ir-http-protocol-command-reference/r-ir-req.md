---
title: req
description: Type de requête. Spécifie le type de données demandé.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
TQID: 'https://experienceleague.adobe.com/UyITy7WNd7wQzOa7UaS4xLgVfjnRwkws2sonnmbaVN0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 950
ht-degree: 3%

---

# req{#req}

Type de requête. Spécifie le type de données demandé.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> de débogage <span class="codeph"> </p> </td> 
  <td class="stentry"> <p>Exécutez les commandes en mode de débogage. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> du contenu </span> </p> </td> 
  <td class="stentry"> <p>Renvoyer des informations sur les objets de la vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>Exécutez les commandes et renvoyez l’image rendue. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> <span class="codeph"> imageprops </p> </td> 
  <td class="stentry"> <p>Renvoyer les propriétés de la vignette spécifiée. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> de carte <span class="codeph"> </p> </td> 
  <td class="stentry"> <p>Renvoie les données de zone cliquable intégrées à la vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> de l’objet <span class="codeph"> </p> </td> 
  <td class="stentry"> <p>Exécutez les commandes et renvoyez l’image rendue masquée à la sélection d’objets active. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> props </span> </p> </td> 
  <td class="stentry"> <p>Exécutez les commandes et renvoyez les propriétés de l’image de réponse. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> userdata </span> </p> </td> 
  <td class="stentry"> <p>Renvoie le contenu de <span class="codeph"> vignette::UserData </span>. </p> </td> 
 </tr> 
</table>

Sauf indication contraire dans les descriptions détaillées, le serveur renvoie des réponses textuelles avec le type MIME &lt;text/plain>.

`debug`

Exécute les commandes spécifiées et renvoie l’image rendue. Si une erreur se produit, les informations d’erreur et de débogage sont renvoyées à la place de l’image d’erreur ( `attribute::ErrorImagePath`).

`contents`

Renvoie une représentation XML de la hiérarchie d&#39;objets dans la vignette, y compris les attributs d&#39;objets sélectionnés. Les autres commandes de la requête sont ignorées.

`img`

Exécute les commandes spécifiées et renvoie l’image rendue. Le format des données de réponse et le type de réponse sont déterminés par `fmt=`.

`imageprops`

Renvoie les propriétés sélectionnées du fichier de vignette ou de l’entrée de catalogue spécifiée dans le chemin d’accès à l’URL. Voir [Propriétés](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) pour une description de la syntaxe de réponse et du type MIME de réponse. Les autres commandes de la requête sont ignorées. Les propriétés suivantes sont renvoyées :

<table id="table_A30296D29B5D43F1B5383A887252C6B4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Propriété </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.expiration </span> </p> </td> 
   <td colname="col2"> <p>Double </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Expiration </span> ou la durée de vie par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>Entier </p> </td> 
   <td colname="col3"> <p>Hauteur pleine résolution en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>Chaîne </p> </td> 
   <td colname="col3"> <p>nom/description du profil associé à cette vignette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.beddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>Boolean </p> </td> 
   <td colname="col3"> <p>1 si le profil associé est incorporé dans la vignette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.</span> PhotoshopPaths incorporées </p> </td> 
   <td colname="col2"> <p>Boolean </p> </td> 
   <td colname="col3"> <p>1 si la vignette contient des données de chemin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>Chaîne </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Modifier </span> ou vide si ce n'est pas une entrée de catalogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td colname="col2"> <p>Énumération </p> </td> 
   <td colname="col3"> <p>Type de pixel de l'image de réponse ; peut être 'CMJN', 'RGB' ou 'BW' (pour les images en niveaux de gris). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>Réel </p> </td> 
   <td colname="col3"> <p>Résolution d’impression par défaut en ppp. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>Chaîne </p> </td> 
   <td colname="col3"> <p>Date/heure de modification (à partir <span class="codeph"> catalogue : </span> TimeStamp ou du fichier de vignette). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>Entier </p> </td> 
   <td colname="col3"> <p>Largeur pleine résolution en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>Chaîne </p> </td> 
   <td colname="col3"> <p>Nom de la vignette (chaîne du nom de l’objet vignette racine). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res </span> </p> </td> 
   <td colname="col2"> <p>Réel </p> </td> 
   <td colname="col3"> <p>Résolution maximale de l'objet en unités de </a> de résolution de matériau <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> (généralement pixels/pouce). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>Réel </p> </td> 
   <td colname="col3"> <p>Résolution moyenne de l'objet en unités de </a> de résolution de matériau <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> (généralement pixels/inc <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> résolution de matériau </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>Réel </p> </td> 
   <td colname="col3"> <p>Résolution minimale de l'objet en unités de </a> de résolution de matériau <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> (généralement pixels/pouce). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>Entier </p> </td> 
   <td colname="col3"> <p>Numéro de version du fichier Vignette. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Renvoie les données de zone cliquable incluses dans la vignette. Par défaut, les données de mappage de tous les groupes les plus éloignés sont renvoyées. Les données de mappage pour tous les groupes les plus internes peuvent être obtenues avec

`req=map&groupLevel=-1`

Les données de mappage ne sont pas mises à l’échelle à `wid=` ou `hei=` ou modifiées. Le type MIME de réponse est `<text/xml>`.

Les données de réponse se composent d’un élément `<map>` contenant un ensemble d’éléments `<area>`, similaires à la balise `<AREA>` d’HTML.

Chaque élément `<area>` comprend les attributs `type=` et `coord=` standard, ainsi qu’un attribut `name=`, spécifiant le nom ou le chemin du groupe de vignettes. Plusieurs éléments de `<area>` portant le même nom sont présents si les masques du groupe d’objets correspondant comportent des régions discontinues.

En plus des attributs par défaut, les vignettes peuvent définir des attributs supplémentaires si elles sont créées. Ces attributs personnalisés sont définis comme des attributs de groupe d’objets. Les noms des attributs personnalisés doivent commencer par `map` pour être inclus dans les éléments `<area>`. Par exemple, si les attributs du groupe incluent `map.href=http://www.scene7.com`, l’élément de `<area>` correspondant inclut `href="http://www.scene7.com"`.

Un document XML avec un élément de `<map>` vide est renvoyé si la vignette n’inclut pas de données de mappage.

`object`

Exécute les commandes spécifiées et renvoie l’image rendue masquée par la sélection d’objets résiduelle (le groupe ou l’objet sélectionné avec la dernière commande `sel=` ou `obj=` dans la requête). Généralement utilisé avec un format d’image prenant en charge la version alpha (voir [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). Si un format d’image non compatible avec la version alpha est utilisé, les zones situées à l’extérieur du masque sont noires.

`props`

Exécute les commandes spécifiées et renvoie les propriétés de vignette et les propriétés de groupe ou d’objet, plutôt que l’image rendue. Voir [Propriétés](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) pour une description de la syntaxe de réponse et du type MIME de réponse. La sélection par défaut s’applique, sauf si `obj=` ou `sel=` est également spécifié (voir [`obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

Les propriétés suivantes peuvent être incluses dans la réponse :

<table id="table_F3ECF0584F6247A2A75C1CAFE1C57A4E"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Propriété </p> </th> 
   <th class="entry"> <p> Type </p> </th> 
   <th class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Couleur de fond de l’image de réponse. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>Entier </p> </td> 
   <td> <p> Hauteur de l’image de réponse en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p>True si le profil ICC est incorporé dans l’image de réponse (voir <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Nom du raccourci du profil associé à l’image de réponse (voir <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p> True si l’image de réponse contient la version alpha. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p> True si l'image de réponse contient des données de chemin (voir <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Type d’image de réponse, peut être « CMJN », « RGB » ou « BW » (pour les images en niveaux de gris). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> Réel </p> </td> 
   <td> <p> Résolution d’impression (dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>Entier, booléen </p> </td> 
   <td> <p> Qualité JPEG et indicateur chroma (voir <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Type MIME de l’image de réponse (voir <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Largeur de l’image de réponse en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Chaîne d’attributs de la sélection en cours. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Nombre d’objets dans la sélection en cours. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Mettre en retrait la valeur de la sélection en cours. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> sélectionner <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Chemin d'accès au nom complet de la sélection d'objets active. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlapping </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> nombre d’objets de chevauchement dans la sélection en cours. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p>Nombre d’objets rendus dans la sélection en cours. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Nombre d’objets texturables dans la sélection en cours. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Affiche/masque le statut de la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Valeur de l'ordre Z du premier objet de chevauchement dans la sélection en cours. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Renvoie le contenu de `vignette::UserData`. Le serveur remplace toutes les occurrences de `'??'` en `vignette::UserData` par des terminaisons de ligne ( `<cr><lf>`). La réponse est formatée en tant que données texte avec le type MIME de réponse défini sur &lt;text/plain>.

Si l’objet spécifié dans le chemin d’accès à l’URL n’est pas résolu en une entrée de mappage de vignette valide, ou si l’`vignette::UserData` est vide, la réponse ne contient qu’un terminateur de ligne ( `CR/LF`).

Toutes les autres commandes de la chaîne de requête sont ignorées.

## Propriétés {#section-e44092e190ff4f6380583e8ed6ea5b0b}

Commande de requête. Peut se produire n’importe où dans la chaîne de requête.

## Par défaut {#section-00c593cbf1af4364b6b78812e6b93c64}

Si l’URL n’inclut pas de chemin d’accès ou de modificateurs d’image, alors :

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Sinon, `req=img`

## Voir aussi {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attribute::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [vignette::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [Properties](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)

