---
description: La diffusion d’images offre un mécanisme de conversion des identifiants d’objet externe en identifiants d’objet (catalogue) spécifiques aux paramètres régionaux. L’application Principale permet de fournir du contenu et du contenu propres aux paramètres régionaux partagés entre plusieurs paramètres régionaux sans que l’application cliente ait besoin de connaître les ID d’objet propres aux paramètres régionaux.
solution: Experience Manager
title: Traduction de l’ID d’objet
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 9%

---


# Traduction de l’ID d’objet{#object-id-translation}

La diffusion d’images offre un mécanisme de conversion des identifiants d’objet externe en identifiants d’objet (catalogue) spécifiques aux paramètres régionaux. L’application Principale permet de fournir du contenu et du contenu propres aux paramètres régionaux partagés entre plusieurs paramètres régionaux sans que l’application cliente ait besoin de connaître les ID d’objet propres aux paramètres régionaux.

L’application peut être écrite en utilisant uniquement des ID d’objet globaux et la diffusion d’images remplace automatiquement les images propres aux paramètres régionaux et tout autre contenu disponible.

*`locale`* est spécifié dans les demandes de diffusion d’images avec la commande `locale=`.

>[!NOTE]
>
>La traduction d’ID d’objet ne s’applique qu’à l’utilisation d’Image Serving basée sur un catalogue. Les noms de fichier ne peuvent pas être traduits.

## Etendue {#section-66fcd5bd467c4eeaa1574583cbe9756d}

Toutes les références aux entrées dans les catalogues d’images, SVG et de contenu statique sont prises en compte pour les polices de traduction et les références de profil ICC ne sont pas traduites. Outre le chemin d&#39;accès *`object`* [!DNL /is/image] et [!DNL /is/static requests], ces commandes et attributs de catalogue peuvent faire l&#39;objet d&#39;une traduction d&#39;ID : `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage` et `attribute::Watermark`.

## Carte de traduction de l’ID {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` définit les règles utilisées par le serveur pour déterminer l’ID du contenu localisé, étant donné que l’ID d’objet générique et la  `locale=` valeur sont entrés.

`attribute::LocaleMap` consiste en une liste de  *paramètres régionaux*  d’entrée (correspondant aux valeurs spécifiées avec  `locale=`), chacun avec un ou plusieurs suffixes de paramètres régionaux de sortie ( `*`locSuffixes`*`).

Par exemple, `attribute::LocaleMap` peut ressembler à ceci :

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

La demande `/is/image/myCat/myImg?locale=de_de` renvoie l&#39;image associée à l&#39;entrée de catalogue `myCat/myImg_D` (en supposant qu&#39;une telle entrée de catalogue existe).

Consultez la description de `attribute::LocaleMap` pour plus de détails.

## Processus de traduction {#section-1f64db17e9f644d88e09853670e14a16}

Dans l’exemple ci-dessus, le serveur commence par rechercher *`locale`* &quot; `de_de`&quot; dans le mappage de traduction d’ID. Il effectue ensuite une itération sur le *`locSuffixes`* associé à cette entrée dans ce cas &quot; `_D`&quot; et &quot;&quot; (suffixe vide). Pour chaque itération, le suffixe est ajouté à l’ID d’image et l’identifiant obtenu est testé pour exister dans le catalogue. Si elle est trouvée, cette entrée de catalogue est utilisée, sinon la suivante est testée. Dans cet exemple, ces entrées sont vérifiées : `myCat/myImg_D` et `myCat/myImg`. Si aucune correspondance n’est trouvée, le serveur renvoie une erreur ou une image par défaut (si elle est configurée).

## Paramètres régionaux inconnus {#section-b2f3c83f2dc845d69b5908107b775537}

Dans l’exemple ci-dessus, `attribute::LocaleMap` inclut un *`locale`* vide qui définit la règle de traduction par défaut, utilisée pour les valeurs `locale=` inconnues (c’est-à-dire celles qui ne sont pas explicitement répertoriées dans la carte de traduction). Si ce mappage de traduction était appliqué à la requête `/is/image/myCat/myImg?locale=ja`, il serait résolu sur `myCat/myImg_E`, s&#39;il existe, ou autrement `myCat/myImg`.

Si un mappage de traduction ne spécifie pas de règle de traduction par défaut, une erreur est renvoyée pour toutes les requêtes avec des valeurs `locale=` inconnues.

## Exemples {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**Recherche à plusieurs niveaux**

Il est souvent souhaitable de regrouper des paramètres régionaux (par exemple, européens, moyen-orientaux, nord-américains) pour répondre aux normes régionales. Cela peut être réalisé avec une recherche à plusieurs niveaux.

Pour cet exemple, nous voulons prendre en charge les collections pour une utilisation occidentale et moyen-orientale. Les deux collections reposent sur la collection d’images génériques, et ajoutent ou modifient toutes deux certaines images. Les deux collections sont ensuite affinées pour des paramètres régionaux spécifiques ( `m1`, `m2` pour deux variantes du Moyen-Orient et `w1`, `w2` et `w3` pour trois paramètres régionaux occidentaux), sauf que les images sont partagées pour `w1` et `w3`. Les paramètres régionaux inconnus sont mappés uniquement à la collection générique et n’ont pas accès aux images spécifiques à un paramètre régional.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

Le tableau suivant illustre les entrées de catalogue à prendre en compte et l&#39;ordre dans lequel elles sont prises en compte pour l&#39;ID d&#39;entrée générique `myImg` :

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
   <td> <p> <span class="codeph"> myImg  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Rechercher des identifiants spécifiques**

Certaines conventions d’appellation des images peuvent ne pas prendre en charge les ID d’image génériques en interne. Les ID génériques de la demande doivent toujours être mappés à un ID spécifique dans le catalogue ; souvent, l’identifiant spécifique exact n’est pas connu.

Pour cet exemple, les images pour toutes les langues peuvent avoir le suffixe `_1`, `_2` ou `_3`. Les images propres aux paramètres régionaux français peuvent avoir le suffixe `_22` ou `_23` et les images propres aux paramètres régionaux allemands peuvent avoir le suffixe `_470` ou `_480`.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

Le tableau suivant illustre les entrées de catalogue prises en compte et l&#39;ordre dans lequel elles sont prises en compte pour l&#39;ID d&#39;entrée générique `myImg` :

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
   <td> <p> <span class="codeph"> de  </span>,  <span class="codeph"> de_at  </span>,  <span class="codeph"> de_de  </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tous les autres </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voir aussi {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribut ::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) ,  [attribut ::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b),  [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb),  [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
