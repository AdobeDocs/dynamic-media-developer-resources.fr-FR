---
description: La diffusion d’images fournit un mécanisme pour traduire les ID d’objet externes en ID d’objet spécifiques aux paramètres régionaux (catalogue). L’application principale fournit du contenu spécifique aux paramètres régionaux et du contenu partagé entre plusieurs paramètres régionaux sans que l’application cliente n’ait besoin de connaître les identifiants d’objet spécifiques aux paramètres régionaux.
solution: Experience Manager
title: Traduction de l’ID d’objet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 2%

---

# Traduction de l’ID d’objet{#object-id-translation}

La diffusion d’images fournit un mécanisme pour traduire les ID d’objet externes en ID d’objet spécifiques aux paramètres régionaux (catalogue). L’application principale fournit du contenu spécifique aux paramètres régionaux et du contenu partagé entre plusieurs paramètres régionaux sans que l’application cliente n’ait besoin de connaître les identifiants d’objet spécifiques aux paramètres régionaux.

L’application peut être écrite en utilisant uniquement des identifiants d’objet globaux. Le service d’images remplace automatiquement les images spécifiques aux paramètres régionaux et tout autre contenu si disponible.

Le *`locale`* est spécifié dans les requêtes de diffusion d’images avec la commande `locale=` .

>[!NOTE]
>
>La traduction de l’ID d’objet s’applique uniquement à l’utilisation catalogue de la diffusion d’images. Les noms de fichier ne peuvent pas être traduits.

## Portée {#section-66fcd5bd467c4eeaa1574583cbe9756d}

Toutes les références aux entrées des catalogues d’images, de SVG et de contenu statique sont prises en compte pour les polices de traduction et les références de profil ICC ne sont pas traduites. En plus des *`object`* dans le chemin d’accès de [!DNL /is/image] et [!DNL /is/static requests], ces commandes et attributs de catalogue sont soumis à la traduction des identifiants : `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage` et `attribute::Watermark`.

## La carte de traduction des identifiants {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` définit les règles utilisées par le serveur pour déterminer l’identifiant du contenu localisé, donné sous forme d’entrées l’identifiant d’objet générique et la valeur de `locale=`.

`attribute::LocaleMap` se compose d’une liste de paramètres régionaux d’entrée *locales* (correspondant aux valeurs spécifiées avec `locale=`), chacun avec aucun ou plusieurs suffixes de paramètres régionaux de sortie ( `*`locSuffixes`*`).

Par exemple, `attribute::LocaleMap` pourrait ressembler à ceci :

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

La requête `/is/image/myCat/myImg?locale=de_de` renvoie l’image associée à l’entrée de catalogue `myCat/myImg_D` (en supposant qu’une telle entrée de catalogue existe).

Pour plus d’informations, consultez la description de `attribute::LocaleMap` .

## Le processus de traduction {#section-1f64db17e9f644d88e09853670e14a16}

Compte tenu de l’exemple ci-dessus, le serveur recherche d’abord le *`locale`* « `de_de` » dans la carte de traduction des identifiants. Il effectue ensuite une itération sur le *`locSuffixes`* associé à cette entrée, dans ce cas « `_D` » et « » (suffixe vide). Pour chaque itération, le suffixe est ajouté à l’ID d’image et l’ID obtenu est testé pour exister dans le catalogue. Si elle est trouvée, cette entrée de catalogue est utilisée, sinon la suivante est testée. Pour cet exemple, les entrées suivantes sont vérifiées : `myCat/myImg_D` et `myCat/myImg`. Si aucune correspondance n’est trouvée, le serveur renvoie une erreur ou une image par défaut (si elle est configurée de la sorte).

## Paramètres régionaux inconnus {#section-b2f3c83f2dc845d69b5908107b775537}

Dans l’exemple ci-dessus, `attribute::LocaleMap` inclut un *`locale`* vide qui définit la règle de traduction par défaut, utilisée pour les valeurs de `locale=` inconnues (c’est-à-dire celles qui ne sont pas explicitement répertoriées dans le mappage de traduction). Si ce mappage de traduction était appliqué au `/is/image/myCat/myImg?locale=ja` de requête, il serait résolu en `myCat/myImg_E`, s’il existe, ou `myCat/myImg`.

Si une carte de traduction ne spécifie pas de règle de traduction par défaut, une erreur est renvoyée pour toutes les requêtes avec des valeurs de `locale=` inconnues.

## Exemples {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**Recherche à plusieurs niveaux**

Il est souvent souhaitable de regrouper les paramètres régionaux (par exemple, européens, moyen-orientaux, nord-américains) pour répondre aux normes régionales. Cela peut être réalisé à l’aide d’une recherche à plusieurs niveaux.

Pour cet exemple, nous voulons prendre en charge les collections destinées à une utilisation en Occident et au Moyen-Orient. Les deux collections reposent sur la collection d’images génériques, et ajoutent ou modifient toutes deux certaines images. Les deux collections sont ensuite affinées pour des paramètres régionaux spécifiques ( `m1`, `m2` pour deux variantes du Moyen-Orient et `w1`, `w2` et `w3` pour trois paramètres régionaux occidentaux), mais les images sont partagées pour `w1` et `w3`. Les paramètres régionaux inconnus sont mappés uniquement à la collection générique et n’ont pas accès aux images spécifiques aux paramètres régionaux.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

Le tableau suivant illustre les entrées de catalogue prises en compte et l’ordre dans lequel elles sont prises en compte pour l’ID d’entrée générique `myImg` :

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>paramètres régionaux</i> </b> </th> 
   <th class="entry"> <b>ID de catalogue à rechercher</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tous les autres </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Rechercher des identifiants spécifiques**

Certaines conventions de dénomination des images peuvent ne pas prendre en charge les identifiants d’image génériques en interne. Les identifiants génériques de la requête doivent toujours être mappés à un identifiant spécifique dans le catalogue. Souvent, l’identifiant spécifique exact peut ne pas être connu.

Pour cet exemple, les images pour toutes les langues peuvent avoir un suffixe `_1`, `_2` ou `_3`. Les images spécifiques aux paramètres régionaux français peuvent avoir un suffixe `_22` ou `_23`, et les images spécifiques aux paramètres régionaux allemands peuvent avoir un suffixe `_470` ou `_480`.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

Le tableau suivant illustre les entrées de catalogue prises en compte et l’ordre dans lequel elles sont prises en compte pour l’ID d’entrée générique `myImg` :

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>paramètres régionaux</i> </b> </th> 
   <th class="entry"> <b>ID de sortie à rechercher</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tous les autres </p> </td> 
   <td> <p> <span class="codeph"> les </span> myImg_1, myImg_2, myImg_3 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voir aussi {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b), [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
