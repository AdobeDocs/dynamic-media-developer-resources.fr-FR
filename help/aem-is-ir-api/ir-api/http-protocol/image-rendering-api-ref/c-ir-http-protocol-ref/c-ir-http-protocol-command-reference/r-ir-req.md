---
description: Type de demande. Indique le type de données demandé.
solution: Experience Manager
title: req
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 4%

---


# req{#req}

Type de demande. Indique le type de données demandé.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> déboguer  </span> </p> </td> 
  <td class="stentry"> <p>Exécutez les commandes en mode débogage. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> contenu </span> </p> </td> 
  <td class="stentry"> <p>Renvoie des informations sur les objets de la vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img  </span> </p> </td> 
  <td class="stentry"> <p>Exécutez les commandes et renvoyez l’image rendue. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops  </span> </p> </td> 
  <td class="stentry"> <p>Renvoie les propriétés de la vignette spécifiée. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> carte </span> </p> </td> 
  <td class="stentry"> <p>Renvoie les données de zone cliquable incorporées dans la vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> objet </span> </p> </td> 
  <td class="stentry"> <p>Exécutez les commandes et renvoyez l’image rendue masquée à la sélection d’objets active. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> props </span> </p> </td> 
  <td class="stentry"> <p>Exécutez les commandes et renvoyez les propriétés de l’image de réponse. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> userdata  </span> </p> </td> 
  <td class="stentry"> <p>Renvoie le contenu de <span class="codeph"> vignette::UserData </span>. </p> </td> 
 </tr> 
</table>

Sauf indication contraire dans les descriptions détaillées, le serveur renvoie des réponses texte de type MIME &lt;text/plain>.

`debug`

Exécute les commandes spécifiées et renvoie l’image rendue. Si une erreur se produit, les informations d&#39;erreur et de débogage sont renvoyées à la place de l&#39;image d&#39;erreur ( `attribute::ErrorImagePath`).

`contents`

Renvoie une représentation XML de la hiérarchie d’objets dans la vignette, y compris les attributs d’objet sélectionnés. Les autres commandes de la requête sont ignorées.

`img`

Exécute les commandes spécifiées et renvoie l’image rendue. Le format des données de réponse et le type de réponse sont déterminés par `fmt=`.

`imageprops`

Renvoie les propriétés sélectionnées du fichier de vignette ou de l’entrée de catalogue spécifiée dans le chemin d’accès de l’URL. Voir [Propriétés](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) pour une description de la syntaxe de réponse et du type MIME de réponse. Les autres commandes de la requête sont ignorées. Les propriétés suivantes sont renvoyées :

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
   <td colname="col1"> <p> <span class="codeph"> image.expiration  </span> </p> </td> 
   <td colname="col2"> <p>Doublon </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Expiration  </span> ou l'heure par défaut à vivre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td colname="col2"> <p>Entier </p> </td> 
   <td colname="col3"> <p>Hauteur de résolution totale en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td colname="col2"> <p>Chaîne </p> </td> 
   <td colname="col3"> <p>nom/description du profil associé à cette vignette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.beddedIccProfile  </span> </p> </td> 
   <td colname="col2"> <p>Boolean </p> </td> 
   <td colname="col3"> <p>1 si le profil associé est incorporé dans la vignette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.bedded PhotoshopPaths  </span> </p> </td> 
   <td colname="col2"> <p>Boolean </p> </td> 
   <td colname="col3"> <p>1 si la vignette incorpore des données de chemin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier  </span> </p> </td> 
   <td colname="col2"> <p>Chaîne </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribut::Modificateur  </span> ou vide si ce n'est pas une entrée de catalogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixTyp  </span> </p> </td> 
   <td colname="col2"> <p>Enum </p> </td> 
   <td colname="col3"> <p>Type de pixel de l'image de réponse ; peut être CMJN, RVB ou BW (pour les images en niveaux de gris). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Résolution d’impression par défaut en ppp. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp  </span> </p> </td> 
   <td colname="col2"> <p>Chaîne </p> </td> 
   <td colname="col3"> <p>Date/heure de modification (à partir du <span class="codeph"> catalogue::TimeStamp </span> ou du fichier de vignette). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td colname="col2"> <p>Entier </p> </td> 
   <td colname="col3"> <p>Largeur en pleine résolution, en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name  </span> </p> </td> 
   <td colname="col2"> <p>Chaîne </p> </td> 
   <td colname="col3"> <p>Nom de la vignette (chaîne de nom de l’objet de vignette racine). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Résolution d’objet maximale en unités <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> de résolution de matériau </a> (généralement pixels/pouce). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Résolution moyenne d'objet en unités <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> de résolution de matériau </a> (généralement en pixels/inc <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> de résolution de matériau </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Résolution d’objet minimale en unités <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> de résolution de matériau </a> (généralement en pixels/pouce). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version  </span> </p> </td> 
   <td colname="col2"> <p>Entier </p> </td> 
   <td colname="col3"> <p>Numéro de version du fichier de vignette. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Renvoie les données de zone cliquable incluses dans la vignette. Par défaut, les données de mappage pour tous les groupes les plus éloignés sont renvoyées. Les données de mappage pour tous les groupes les plus internes peuvent être obtenues avec

`req=map&groupLevel=-1`

Les données de mappage ne sont pas mises à l’échelle sur `wid=` ou `hei=` ou modifiées d’une autre manière. Le type MIME de réponse est `<text/xml>`.

Les données de réponse se composent d’un élément `<map>` contenant un ensemble d’éléments `<area>`, similaire à la balise HTML `<AREA>`.

Chaque élément `<area>` comprend les attributs standard `type=` et `coord=`, ainsi qu&#39;un attribut `name=`, en spécifiant le nom du groupe de vignettes ou le chemin d&#39;accès au nom. Plusieurs éléments `<area>` portant le même nom seront présents si les masques du groupe d’objets correspondant comportent des régions discontinues.

Outre les attributs par défaut, les vignettes peuvent définir des attributs supplémentaires si elles sont créées. Ces attributs personnalisés sont définis comme des attributs de groupe d’objets. Les noms des attributs personnalisés doivent commencer par `map`. à inclure dans les éléments `<area>`. Par exemple, si les attributs de groupe incluent `map.href=http://www.scene7.com`, l’élément `<area>` correspondant inclut `href="http://www.scene7.com"`.

Un document XML avec un élément `<map>` vide est renvoyé si la vignette n’inclut pas de données de mappage.

`object`

Exécute les commandes spécifiées et renvoie l’image rendue masquée par la sélection d’objets résiduelle (groupe ou objet sélectionné avec la dernière commande `sel=` ou `obj=` dans la requête). Habituellement utilisé avec un format d’image qui prend en charge alpha (voir [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). Si un format d’image n’est pas compatible avec le format alpha, les zones extérieures au masque sont noires.

`props`

Exécute les commandes spécifiées et renvoie les propriétés de vignette et de groupe ou d’objet, plutôt que l’image rendue. Voir [Propriétés](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) pour une description de la syntaxe de réponse et du type MIME de réponse. La sélection par défaut s&#39;applique à moins que `obj=` ou `sel=` ne soit également spécifié (voir [ `obj=` ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

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
   <td> <p> <span class="codeph"> image.bgc  </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Couleur d’arrière-plan de l’image de réponse. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td> <p>Entier </p> </td> 
   <td> <p> Hauteur de l’image de réponse en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed  </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p>True si le profil ICC sera incorporé à l’image de réponse (voir <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Nom de raccourci du profil associé à l’image de réponse (voir <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p> True si l’image de réponse contient alpha. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p> True si l’image de réponse contient des données de chemin d’accès (voir <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp  </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Le type d’image de réponse peut être CMJN, RVB ou BW (pour les images en niveaux de gris). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td> <p> Real </p> </td> 
   <td> <p> Résolution d’impression (ppp) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality  </span> </p> </td> 
   <td> <p>Entier, booléen </p> </td> 
   <td> <p> Qualité JPEG et indicateur de chroma (voir <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type  </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Type Mime pour l’image de réponse (voir <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Largeur de l’image de réponse en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes  </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Chaîne d’attributs pour la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count  </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Nombre d’objets dans la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selected.ident  </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Retrait de la valeur de la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select  <span class="codeph"> selection.attributes  </span>ion.name  </span> </p> </td> 
   <td> <p> Chaîne </p> </td> 
   <td> <p> Chemin d’accès au nom complet de la sélection d’objets active. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlapping  </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> nombre d’objets de chevauchement dans la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable  </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p>Nombre d’objets à rendre dans la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable  </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Nombre d’objets de texte dans la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible  </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Afficher/masquer l’état actuel de la sélection actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder  </span> </p> </td> 
   <td> <p> Entier </p> </td> 
   <td> <p> Ordre Z du premier objet de chevauchement dans la sélection actuelle. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Renvoie le contenu de `vignette::UserData`. Le serveur remplacera toutes les occurrences de `'??'` dans `vignette::UserData` par des terminateurs de ligne ( `<cr><lf>`). La réponse est formatée sous la forme de données texte, le type MIME de la réponse étant défini sur &lt;text/plain>.

Si l’objet spécifié dans le chemin d’accès de l’URL ne correspond pas à une entrée de mappage de vignettes valide ou si `vignette::UserData` est vide, la réponse contient uniquement un terminateur de ligne ( `CR/LF`).

Toutes les autres commandes de la chaîne de requête sont ignorées.

## Propriétés {#section-e44092e190ff4f6380583e8ed6ea5b0b}

Commande Request. Peut se produire n’importe où dans la chaîne de requête.

## Par défaut {#section-00c593cbf1af4364b6b78812e6b93c64}

Si l’URL n’inclut pas de chemin d’accès à l’image ou de modificateurs, alors :

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Sinon, `req=img`

## Voir aussi {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) ,  [attribut::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0),  [vignette::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85),  [propriétés](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
