---
description: La localisation de chaînes de texte permet aux catalogues d’images de contenir plusieurs représentations spécifiques aux paramètres régionaux pour la même valeur de chaîne.
solution: Experience Manager
title: Localisation de chaîne de texte
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 3%

---


# Localisation de chaîne de texte {#text-string-localization}

La localisation de chaînes de texte permet aux catalogues d’images de contenir plusieurs représentations spécifiques aux paramètres régionaux pour la même valeur de chaîne.

Le serveur retourne au client la représentation correspondant au paramètre régional spécifié par `locale=`, évitant ainsi la localisation côté client et permettant aux applications de changer de paramètre régional simplement en envoyant la valeur `locale=` appropriée avec les requêtes de texte IS.

## Etendue {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

La localisation de chaîne de texte est appliquée à tous les éléments de chaîne qui incluent le jeton de localisation ` ^loc= *`locId`*^` dans les champs de catalogue suivants :

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Champ Catalogue</b> </th> 
   <th class="entry"> <b>Elément de chaîne dans le champ</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::ImageSet  </span> </p> </td> 
   <td> <p>Tout sous-élément contenant une chaîne convertible (délimité par toute combinaison de séparateurs ',' ';' ' :' et/ou le début/la fin du champ). </p> <p> Une valeur de couleur <span class="codeph"> 0xrgbb </span> au début d'un champ localisable est exclue de la localisation et transmise sans modification. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::Carte  </span> </p> </td> 
   <td> <p>Toute valeur d’attribut entre guillemets simples ou doublons, à l’exception des valeurs des attributs <span class="codeph"> coords= </span> et <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue::Cibles  </span> </p> </td> 
   <td> <p>Valeur de toute cible <span class="codeph">.*.label </span> et <span class="codeph"> cible.*.userdata </span> propriété. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::UserData  </span> </p> </td> 
   <td> <p>Valeur d’une propriété. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Syntaxe de chaîne {#section-d12320edf300409f8e17565b143acafc}

Les éléments *`string`* activés pour la localisation dans le catalogue d’images se composent d’une ou de plusieurs chaînes localisées, chacune précédée d’un jeton de localisation.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement  </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc=  <span class="varname"> locStr  </span> ^  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID de paramètre régional interne pour la chaîne <span class="varname"> localizedString </span> qui suit cet élément <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString  </span> </span> </p> </td> 
  <td class="stentry"> <p>Chaîne localisée. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString  </span> </span> </p> </td> 
  <td class="stentry"> <p>Chaîne à utiliser pour les paramètres régionaux inconnus. </p> </td> 
 </tr> 
</table>

*`locId`* doit être ASCII et ne peut pas inclure &#39;^&#39;.

&#39;^&#39; peut se produire n&#39;importe où dans les sous-chaînes avec ou sans codage HTTP. Le serveur correspond à l’ensemble du modèle *`localizationToken`* `^loc=locId^` pour séparer les sous-chaînes.

*`stringElements`* qui ne comportent pas au moins un élément  *`localizationToken`* ne sont pas considérés comme localisations.

## Carte de traduction {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` définit les règles utilisées par le serveur pour déterminer lequel  *`localizedStrings`* renvoyer au client. Il se compose d’une liste d’entrée *`locales`* (correspondant aux valeurs spécifiées avec `locale=`), chacune n’ayant aucun ou plusieurs identifiants de paramètres régionaux internes ( *`locId`*). Par exemple :

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Les valeurs *`locId`* vides indiquent que *`defaultString`* doit être renvoyé, le cas échéant.

Consultez la description de `attribute::LocaleStrMap` pour plus de détails.

## Processus de traduction {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Compte tenu de l’exemple de mappage de traduction ci-dessus et de la requête `/is/image/myCat/myItem?req=&locale=nl`, le serveur commence par rechercher &quot; `nl`&quot; dans le mappage de paramètres régionaux. L&#39;entrée correspondante `nl,N` indique que pour chaque *`stringElement`*, le *`localizedString`* marqué par `^loc=N^` doit être renvoyé. Si *`localizationToken`* n&#39;est pas présent dans *`stringElement`*, une valeur vide est renvoyée.

Supposons que `catalog::UserData` pour `myCat/myItem` contienne ce qui suit (sauts de ligne insérés pour plus de clarté) :

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Le serveur renvoie les éléments suivants en réponse à notre exemple de demande :

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Paramètres régionaux inconnus {#section-26dfeefbd60345de94bbfeaaf7741223}

Dans l’exemple ci-dessus, `attribute::LocaleStrMap` comporte une entrée avec une valeur *`locale`* vide. Le serveur utilise cette entrée pour gérer toutes les valeurs `locale=` qui ne sont pas explicitement spécifiées autrement dans le mappage de traduction.

L&#39;exemple de mappage de traduction indique que dans un tel cas, *`defaultString`* doit être renvoyé si disponible. Ainsi, les éléments suivants seraient renvoyés si cette carte de traduction était appliquée à la demande `/is/image/myCat/myItem?req=&locale=ja` :

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Exemples {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Familles de langues**

Plusieurs valeurs *`locId`* peuvent être associées à chaque *`locale`* dans la carte de traduction. Cela permet de prendre en charge des variations spécifiques à un pays ou à une région (par exemple Anglais américain ou Anglais britannique) pour sélectionner *`stringElements`* tout en gérant la plupart des contenus avec des paramètres régionaux de base communs (par exemple Anglais international).

Pour notre exemple, nous voulons ajouter la prise en charge de l’anglais spécifique aux États-Unis ( `*`locId`* EUS`) et de l’anglais spécifique au Royaume-Uni ( `*`locId`* EUK`), afin de prendre en charge l’orthographe alternative occasionnelle. Si l&#39;EUK ou l&#39;EUS n&#39;existent pas, nous retournions à E. De même, les variantes allemandes spécifiques à l&#39;Autriche ( `DAT`) pourraient être disponibles lorsque cela est nécessaire tout en renvoyant l&#39;allemand commun *`localizedStrings`* (marqué par `D`) la plupart du temps.

`attribute::LocaleStrMap` ressemblerait à ceci :

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

Le tableau suivant décrit la sortie de certaines combinaisons *`stringElement`* et *`locale`* représentatives :

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>locale</i> </th> 
   <th class="entry"> <p>Chaîne de sortie </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^Anglais^loc=D^Allemand  </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>Allemand </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^Allemand^loc=DAT^Autrichien  </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>Anglais-Royaume-Uni </p> <p>Allemand </p> <p>Autrichien </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^Anglais^loc=USE^Anglais-US^loc=D^Allemand^loc=DDE^Deutsch  </span> </p> <p> Notez que pour cet exemple, le DDE <span class="varname"> locId </span> n'existe pas dans l'attribut <span class="codeph">::LocaleStrMap </span> et que la sous-chaîne associée à cet <span class="varname"> locId </span> n'est jamais renvoyée. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>Anglais-Etats-Unis </p> <p>Allemand </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

