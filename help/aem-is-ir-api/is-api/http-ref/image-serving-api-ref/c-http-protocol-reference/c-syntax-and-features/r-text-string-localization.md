---
title: Localisation de chaîne de texte
description: La localisation de chaîne de texte permet aux catalogues d’images de contenir plusieurs représentations spécifiques aux paramètres régionaux pour la même valeur de chaîne.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
TQID: 'https://experienceleague.adobe.com/iT-q5yLQijvkYDB0xOq3E6r1k3DIbU9BWu3Jkqs8wUI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 672
ht-degree: 1%

---

# Localisation de chaîne de texte{#text-string-localization}

La localisation de chaîne de texte permet aux catalogues d’images de contenir plusieurs représentations spécifiques aux paramètres régionaux pour la même valeur de chaîne.

Le serveur renvoie au client la représentation correspondant au paramètre régional spécifié avec `locale=`, en évitant la localisation côté client et en permettant aux applications de changer de paramètre régional simplement en envoyant la valeur de `locale=` appropriée avec les requêtes de texte IS.

## Portée {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

La localisation des chaînes de texte est appliquée à tous les éléments de chaîne qui incluent le jeton de localisation ` ^loc= *`locId`*^` dans les champs de catalogue suivants :

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Champ catalogue</b> </th> 
   <th class="entry"> <b>Élément de chaîne dans le champ</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>Tout sous-élément contenant une chaîne traduisible (délimitée par n’importe quelle combinaison de séparateurs « , » ; « : » et/ou le début/la fin du champ). </p> <p> Une valeur de couleur de </span> 0xrrggbb <span class="codeph"> au début d’un champ localisable est exclue de la localisation et transmise sans modification. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>Toute valeur d’attribut entre guillemets simples ou doubles, à l’exception des valeurs des attributs coords <span class="codeph">= </span> et Forme <span class="codeph">= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Targets </span> </p> </td> 
   <td> <p>La valeur de tout </span> target.*.label <span class="codeph"> et <span class="codeph"> propriété target.*.userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>La valeur de n’importe quelle propriété. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Syntaxe de chaîne {#section-d12320edf300409f8e17565b143acafc}

Les éléments de *`string`* activés pour la localisation dans le catalogue d’images se composent d’une ou de plusieurs chaînes localisées, chacune précédée d’un jeton de localisation.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>Identifiant de paramètre régional interne pour le </span> localizedString <span class="varname"> suivant ce </span> localizationToken <span class="varname">. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span> </span> </p> </td> 
  <td class="stentry"> <p>Chaîne localisée. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span> </span> </p> </td> 
  <td class="stentry"> <p>Chaîne à utiliser pour les paramètres régionaux inconnus. </p> </td> 
 </tr> 
</table>

Le *`locId`* doit être de type ASCII et ne peut pas inclure « ^ ».

Le caractère « ^ » peut se produire n’importe où dans les sous-chaînes, avec ou sans codage HTTP. Le serveur fait correspondre l’ensemble du modèle de `^loc=locId^` *`localizationToken`* à des sous-chaînes distinctes.

Les *`stringElements`*, qui n’incluent pas au moins un *`localizationToken`*, ne sont pas pris en compte pour la localisation.

## La carte de traduction {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` définit les règles utilisées par le serveur pour déterminer les *`localizedStrings`* à renvoyer au client. Elle comprend une liste de *`locales`* d’entrée (correspondant aux valeurs spécifiées avec `locale=`), chacun avec aucun ou plusieurs identifiants de paramètres régionaux internes ( *`locId`*). Par exemple :

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Des valeurs de *`locId`* vides indiquent que le *`defaultString`* doit être renvoyé, le cas échéant.

Pour plus d’informations, consultez la description de `attribute::LocaleStrMap` .

## Le processus de traduction {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Compte tenu de l’exemple de mappage de traduction ci-dessus et du `/is/image/myCat/myItem?req=&locale=nl` de requête, le serveur recherche d’abord « `nl` » dans le mappage des paramètres régionaux. La `nl,N` d’entrée correspondante indique que pour chaque *`stringElement`*, les *`localizedString`* marquées avec `^loc=N^` doivent être renvoyées. Si ce *`localizationToken`* n’est pas présent dans le *`stringElement`*, une valeur vide est renvoyée.

Supposons que `catalog::UserData` pour `myCat/myItem` contienne les éléments suivants (des sauts de ligne sont insérés pour plus de clarté) :

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Le serveur renvoie les éléments suivants en réponse à l’exemple de requête :

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Paramètres régionaux inconnus {#section-26dfeefbd60345de94bbfeaaf7741223}

Dans l’exemple ci-dessus, `attribute::LocaleStrMap` comporte une entrée avec une valeur de *`locale`* vide. Le serveur utilise cette entrée pour gérer toutes les valeurs de `locale=` qui ne sont pas explicitement spécifiées autrement dans la carte de traduction.

L’exemple de carte de traduction spécifie que, dans ce cas, la *`defaultString`* doit être renvoyée, si elle est disponible. Par conséquent, les éléments suivants sont renvoyés si ce mappage de traduction est appliqué au `/is/image/myCat/myItem?req=&locale=ja` de requête :

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Exemples {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Familles de langues**

Plusieurs valeurs de *`locId`* peuvent être associées à chaque *`locale`* dans la carte de traduction. En effet, il permet de prendre en charge des variations spécifiques à un pays ou à une région (par exemple, l’anglais des États-Unis par rapport à l’anglais du Royaume-Uni) pour certains *`stringElements`*, tout en gérant la plupart des contenus avec des paramètres régionaux de base communs (par exemple, l’anglais international).

Dans cet exemple, la prise en charge est ajoutée pour l’anglais spécifique aux États-Unis ( `*`locId`* EUS`) et pour l’anglais spécifique au Royaume-Uni ( `*`locId`* EUK`), afin de prendre en charge une autre orthographe occasionnelle. S’il n’existe pas d’EUK ou d’EUS, il revient à E. De même, des variantes allemandes spécifiques à l’Autriche ( `DAT`) pourraient être mises à disposition si nécessaire, tout en renvoyant des *`localizedStrings`* allemandes communes (marquées `D`) la plupart du temps.

Voici à quoi devrait ressembler le `attribute::LocaleStrMap` :

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

Le tableau suivant décrit les résultats de certaines combinaisons de *`stringElement`* et de *`locale`* représentatives :

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>paramètres régionaux</i> </th> 
   <th class="entry"> <p>Chaîne de sortie </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^Anglais^loc=D^Allemand </span> </p> </td> 
   <td> <p> en, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>Allemand </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^anglais^loc=UKE^UK-English^loc=D^allemand^loc=DAT^autrichien </span> </p> </td> 
   <td> <p> en, en_us </p> <p> fr_fr </p> <p> de, de_de </p> <p>de_at </p> <p>tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>UK-Anglais </p> <p>Allemand </p> <p>Autrichien </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> Pour cet exemple, le DDE <span class="varname"> locId </span> n’existe pas dans <span class="codeph">’attribut::LocaleStrMap </span>, et la sous-chaîne associée à ce </span> locId <span class="varname"> n’est donc jamais renvoyée. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>Anglais (États-Unis) </p> <p>Allemand </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
