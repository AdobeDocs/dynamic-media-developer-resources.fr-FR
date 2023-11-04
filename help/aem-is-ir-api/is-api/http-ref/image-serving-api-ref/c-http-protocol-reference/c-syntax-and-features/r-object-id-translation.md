---
description: La diffusion d’images fournit un mécanisme pour traduire les identifiants d’objet externe en identifiants d’objet (catalogue) spécifiques aux paramètres régionaux. L’application principale est de fournir du contenu et du contenu propres aux paramètres régionaux partagés entre plusieurs paramètres régionaux sans que l’application cliente ait besoin de connaître les ID d’objet spécifiques aux paramètres régionaux.
solution: Experience Manager
title: Traduction de l’ID d’objet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 9%

---

# Traduction de l’ID d’objet{#object-id-translation}

La diffusion d’images fournit un mécanisme pour traduire les identifiants d’objet externe en identifiants d’objet (catalogue) spécifiques aux paramètres régionaux. L’application principale est de fournir du contenu et du contenu propres aux paramètres régionaux partagés entre plusieurs paramètres régionaux sans que l’application cliente ait besoin de connaître les ID d’objet spécifiques aux paramètres régionaux.

L’application peut être écrite à l’aide des ID d’objet global uniquement et du serveur d’images remplace automatiquement les images propres aux paramètres régionaux et tout autre contenu, le cas échéant.

La variable *`locale`* est spécifié dans les demandes de diffusion d’images avec le `locale=` .

>[!NOTE]
>
>La traduction de l’ID d’objet s’applique uniquement à l’utilisation du serveur d’images basée sur les catalogues. Les noms de fichier ne peuvent pas être traduits.

## Portée {#section-66fcd5bd467c4eeaa1574583cbe9756d}

Toutes les références aux entrées dans les catalogues d’images, de SVG et de contenu statique sont prises en compte pour les polices de traduction et les références de profil ICC ne sont pas traduites. En plus de la variable *`object`* dans le chemin d’accès de [!DNL /is/image] et [!DNL /is/static requests], ces commandes et attributs de catalogue sont soumis à la traduction des identifiants : `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage`, et `attribute::Watermark`.

## Carte de traduction des identifiants {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` définit les règles utilisées par le serveur pour déterminer l’identifiant du contenu localisé, étant donné que en entrée, l’identifiant d’objet générique et la variable `locale=` .

`attribute::LocaleMap` se compose d’une liste d’entrées. *locales* (correspondant aux valeurs spécifiées avec `locale=`), chacun sans suffixe de paramètres régionaux de sortie ( `*`locSuffixes`*`).

Par exemple : `attribute::LocaleMap` peut se présenter comme suit :

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

La requête `/is/image/myCat/myImg?locale=de_de` renvoie l’image associée à l’entrée de catalogue. `myCat/myImg_D` (en supposant qu’une telle entrée de catalogue existe).

Reportez-vous à la description de `attribute::LocaleMap` pour plus d’informations.

## Processus de traduction {#section-1f64db17e9f644d88e09853670e14a16}

Dans l’exemple ci-dessus, le serveur commence par rechercher la variable *`locale`* &quot; `de_de`&quot; dans la carte de traduction des identifiants. Il effectue ensuite une itération sur l’objet *`locSuffixes`* associé à cette entrée dans ce cas &quot; `_D`&quot; et &quot;&quot; (suffixe vide). Pour chaque itération, le suffixe est ajouté à l’ID de l’image et l’ID résultant est testé pour exister dans le catalogue. Si elle est trouvée, cette entrée de catalogue est utilisée, sinon la prochaine est testée. Pour cet exemple, les entrées suivantes sont vérifiées : `myCat/myImg_D`, et `myCat/myImg`. Si aucune correspondance n’est trouvée, le serveur renvoie une erreur ou une image par défaut (si elle est configurée).

## Paramètres régionaux inconnus {#section-b2f3c83f2dc845d69b5908107b775537}

Dans l’exemple ci-dessus, `attribute::LocaleMap` inclut une valeur vide *`locale`* qui définit la règle de traduction par défaut, utilisée pour les variables inconnues `locale=` (c’est-à-dire, ceux qui ne sont pas explicitement répertoriés dans la carte de traduction). Si cette carte de traduction a été appliquée à la requête `/is/image/myCat/myImg?locale=ja`, la résolution est `myCat/myImg_E`, s’il existe, ou autrement `myCat/myImg`.

Si une carte de traduction ne spécifie pas de règle de traduction par défaut, une erreur est renvoyée pour toutes les requêtes avec une valeur inconnue. `locale=` valeurs.

## Exemples {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**Recherche à plusieurs niveaux**

Il est souvent souhaitable de regrouper des paramètres régionaux (par exemple, européens, moyen-orientaux, nord-américains) pour répondre aux normes régionales. Cela peut être réalisé avec une recherche à plusieurs niveaux.

Pour cet exemple, nous voulons prendre en charge les collections pour une utilisation occidentale et moyen-orientale. Les deux collections reposent sur la collection d’images génériques, et ajoutent ou modifient toutes deux certaines images. Les deux collections sont ensuite affinées pour des paramètres régionaux spécifiques ( `m1`, `m2` pour deux variantes du Moyen-Orient, et `w1`, `w2`, et `w3` pour trois paramètres régionaux occidentaux), sauf que les images sont partagées pour `w1` et `w3`. Les paramètres régionaux inconnus sont mappés uniquement à la collection générique et n’ont pas accès aux images spécifiques à un paramètre régional.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

Le tableau suivant illustre les entrées de catalogue prises en compte et l’ordre dans lequel elles sont prises en compte pour l’ID d’entrée générique. `myImg`:

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
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

**Recherche d’identifiants spécifiques**

Certaines conventions de dénomination d’image peuvent ne pas prendre en charge les ID d’image génériques en interne. Les identifiants génériques de la requête doivent toujours être mappés à un identifiant spécifique dans le catalogue ; il arrive souvent que l’identifiant spécifique exact ne soit pas connu.

Pour cet exemple, les images pour toutes les langues peuvent avoir `_1`, `_2`, ou `_3` suffixe. Les images propres aux paramètres régionaux français peuvent avoir `_22` ou `_23` suffixe et les images spécifiques aux paramètres régionaux allemands peuvent avoir `_470` ou `_480` suffixe.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

Le tableau suivant illustre les entrées de catalogue prises en compte et l’ordre dans lequel elles sont prises en compte pour l’ID d’entrée générique. `myImg`:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>ID de sortie à rechercher</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tous les autres </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voir aussi {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b), [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
