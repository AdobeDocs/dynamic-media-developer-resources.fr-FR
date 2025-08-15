---
title: Req
description: Type de demande. Spécifie le type de données demandé.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 3%

---

# Req{#req}

Type de demande. Spécifie le type de données demandé.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> déboguer </span> </p> </td> 
  <td class="stentry"> <p>Exécutez les commandes en mode débogage. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> contenu </span> </p> </td> 
  <td class="stentry"> <p>Renvoie des informations sur les objets figurant dans le fichier vignette </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>Exécuter des commandes et renvoyer l’image rendue. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops </span> </p> </td> 
  <td class="stentry"> <p>Renvoie les propriétés de la vignette spécifiée. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> carte </span> </p> </td> 
  <td class="stentry"> <p>Renvoie les données de zone cliquable incorporées dans le vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> objet </span> </p> </td> 
  <td class="stentry"> <p>Exécuter les commandes et renvoyer l’image rendue masquée à la sélection d’objet en cours. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> accessoires </span> </p> </td> 
  <td class="stentry"> <p>Commandes d’exécution et propriétés de renvoi de l’image de réponse. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Données utilisateur </span> </p> </td> 
  <td class="stentry"> <p>Renvoie le contenu de <span class="codeph"> vignette ::UserData </span>. </p> </td> 
 </tr> 
</table>

Sauf indication contraire dans les descriptions détaillées, le serveur renvoie des réponses textuelles de type MIME &lt;text lain=&quot;&quot;>.&lt;/text>

`debug`

Exécute les commandes spécifiées et renvoie l’image rendue. Si une erreur survient, les informations d’erreur et de débogage sont renvoyées à la place de l’image d’erreur ( `attribute::ErrorImagePath`).

`contents`

Renvoie une représentation XML de la hiérarchie d’objets dans la vignette, y compris les attributs d’objet sélectionnés. Les autres commandes de la requête sont ignorées.

`img`

Exécute les commandes spécifiées et renvoie l’image rendue. Le format et le type de données de réponse sont déterminés par `fmt=`.

`imageprops`

Renvoie les propriétés sélectionnées du fichier de vignette ou de l’entrée de catalogue spécifiées dans le chemin d’URL. Voir [Propriétés](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) pour obtenir une description de la syntaxe de réponse et du type MIME de réponse. Les autres commandes de la requête sont ignorées. Les propriétés suivantes sont renvoyées :

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
   <td colname="col3"> <p> <span class="codeph"> attribute ::Expiration </span> ou la durée de vie par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>Entier </p> </td> 
   <td colname="col3"> <p>Hauteur pleine résolution en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>Chaîne </p> </td> 
   <td colname="col3"> <p>Nom/description du profil associé à cette vignette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>Boolean </p> </td> 
   <td colname="col3"> <p>1 si le profil associé est incorporé dans le fichier vignette ; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PhotoshopPaths image.embedded </span> </p> </td> 
   <td colname="col2"> <p>Boolean </p> </td> 
   <td colname="col3"> <p>1 si la vignette inclut des données de chemin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Modificateur d’image. </span> </p> </td> 
   <td colname="col2"> <p>Chaîne </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute ::Modifier </span> ou vide s’il ne s’agit pas d’une entrée de catalogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td colname="col2"> <p>Enum </p> </td> 
   <td colname="col3"> <p>Type de pixels de l’image de réponse ; peut être « CMJN », « RVB » ou « BW » (pour les images en niveaux de gris). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>Réel </p> </td> 
   <td colname="col3"> <p>Résolution d’impression par défaut en ppp. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>Chaîne </p> </td> 
   <td colname="col3"> <p>Date/heure de modification (à partir de catalog ::TimeStamp ou du <span class="codeph"> fichier de vignette </span> ). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>Entier </p> </td> 
   <td colname="col3"> <p>Largeur pleine résolution en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>Chaîne </p> </td> 
   <td colname="col3"> <p>Nom de la vignette (chaîne de nom de l’objet vignette racine). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res </span> </p> </td> 
   <td colname="col2"> <p>Réel </p> </td> 
   <td colname="col3"> <p>Résolution maximale de l’objet en <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> unités de résolution </a> de matériau (généralement pixels/pouce). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>Réel </p> </td> 
   <td colname="col3"> <p>Résolution moyenne de l’objet en <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> unités de résolution </a> de matériau (généralement pixels/résolution <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> de matériau </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>Réel </p> </td> 
   <td colname="col3"> <p>Résolution minimale de l’objet en <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> unités de résolution </a> de matériau (généralement pixels/pouce). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>Entier </p> </td> 
   <td colname="col3"> <p>Numéro de version du fichier vignette. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Renvoie les données de zone cliquable incluses dans la vignette. Par défaut, les données cartographiques de tous les groupes périphériques sont renvoyées. Les données cartographiques pour tous les groupes les plus internes peuvent être obtenues en utilisant

`req=map&groupLevel=-1`

Les données cartographiques ne sont ni mises à l’échelle ni `wid=` modifiées d’une `hei=` autre manière. Le type MIME de réponse est `<text/xml>`.

Les données de réponse sont constituées d’un `<map>` élément contenant un ensemble d’éléments `<area>` , similaire à la balise HTML `<AREA>` .

Chaque `<area>` élément inclut la norme `type=` et `coord=` les attributs, ainsi qu’un attribut, spécifiant le nom du groupe de vignettes ou le chemin d’accès `name=` au nom. Plusieurs `<area>` éléments portant le même nom sont présents si les masques du groupe d’objets correspondant ont des régions discontinues.

Outre les attributs par défaut, les vignettes peuvent définir des attributs supplémentaires, le cas échéant. Ces attributs personnalisés sont définis en tant qu’attributs de groupe d’objets. Les noms des attributs personnalisés doivent commencer par `map` pour être inclus dans les `<area>` éléments. Par exemple, si les attributs de groupe incluent `map.href=http://www.scene7.com`, l’élément correspondant `<area>` inclut `href="http://www.scene7.com"`.

Un document XML avec un élément vide `<map>` est renvoyé si la vignette n’inclut pas de données cartographiques.

`object`

Exécute les commandes spécifiées et renvoie l’image rendue masquée par la sélection d’objet résiduel (le groupe ou l’objet sélectionné avec la dernière commande ou `sel=` la dernière `obj=` commande dans la requête). Généralement utilisé avec un format d’image prenant en charge alpha (voir [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). Si un format d’image ne prenant pas en charge l’alpha est utilisé, les zones à l’extérieur du masque sont noires.

`props`

Exécute les commandes spécifiées et renvoie les propriétés de vignette et les propriétés de groupe ou d’objet, plutôt que l’image rendue. Voir [Propriétés](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) pour obtenir une description de la syntaxe de réponse et du type MIME de réponse. La sélection par défaut s’applique sauf indication `obj=` `sel=` contraire (voir [`obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

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
   <td> <p> Couleur d’arrière-plan de l’image de réponse. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>Entier </p> </td> 
   <td> <p> Hauteur de l’image de réponse en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p>True si le profil ICC est incorporé dans l’image de réponse (voir <span class="codeph"> iccEmbed= <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> </a>).</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Nom du raccourci du profil associé à l’image de réponse (voir <span class="codeph"> icc= <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> </a>).</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p> True si l’image de réponse inclut une valeur alpha. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p> Valeur True si l’image de réponse comprend des données de chemin (voir <span class="codeph"> pathEmbed= <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> </a>).</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Type d’image de réponse, peut être « CMJN », « RVB » ou « BW » (pour les images en niveaux de gris) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> Réel </p> </td> 
   <td> <p> Résolution d’impression (ppp) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>Nombre entier, booléen </p> </td> 
   <td> <p> Qualité JPEG et drapeau chromatique (voir <span class="codeph"> qlt= <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> </a>)</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Type Mime pour l’image de réponse (voir <span class="codeph"> fmt= <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> </a>).</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Largeur de l’image de réponse en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Chaîne d’attributs pour la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Nombre d’objets dans la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Met la valeur de la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Sélectionnez <span class="codeph"> selection.attributes </span>, ion.name </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Nom complet de la sélection de l’objet sélectionné. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlapping </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Nombre d’objets de chevauchement dans la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p>Nombre d’objets pouvant faire l’objet d’un rendu dans la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Nombre d’objets texturables dans la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Affichage/masquage actuel de l’état de la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Valeur d’ordre Z du premier objet de chevauchement de la sélection actuelle. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Renvoie le contenu de `vignette::UserData`. Le serveur remplace toutes les occurrences de par `'??'` des terminateurs de `vignette::UserData` ligne ( `<cr><lf>`). La réponse est sous forme de données texte avec le type MIME de réponse défini sur &lt;text lain=&quot;&quot;>.&lt;/text>

Si l’objet spécifié dans le chemin d’accès à l’URL n’est pas résolu en tant qu’entrée de mappage de vignette valide, ou si le champ `vignette::UserData` est vide, la réponse contient uniquement un terminateur de ligne ( `CR/LF`).

Toutes les autres commandes de la chaîne de requête sont ignorées.

## Propriétés {#section-e44092e190ff4f6380583e8ed6ea5b0b}

Commande Request. Peut se produire n’importe où dans la chaîne de requête.

## Par défaut {#section-00c593cbf1af4364b6b78812e6b93c64}

Si l’URL n’inclut pas de chemin d’accès ou de modificateurs d’image, alors :

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Autrement `req=img`

## Voir aussi {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attribute ::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [vignette ::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [Propriétés](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
