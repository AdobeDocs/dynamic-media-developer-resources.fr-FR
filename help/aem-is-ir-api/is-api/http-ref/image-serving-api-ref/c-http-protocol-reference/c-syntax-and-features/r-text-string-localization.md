---
title: Localisation de la chaîne de texte
description: La localisation de la chaîne de texte permet aux catalogues d’images de contenir plusieurs représentations locales pour la même valeur de chaîne.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 3%

---

# Localisation de la chaîne de texte{#text-string-localization}

La localisation de la chaîne de texte permet aux catalogues d’images de contenir plusieurs représentations locales pour la même valeur de chaîne.

Le serveur renvoie au client la représentation correspondant au paramètre régional spécifié avec `locale=`, en évitant la localisation côté client et en permettant aux applications de changer de paramètre régional simplement en envoyant le `locale=` avec les requêtes de texte IS.

## Portée {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

La localisation de la chaîne de texte est appliquée à tous les éléments de chaîne qui incluent le jeton de localisation ` ^loc= *`locId`*^` dans les champs de catalogue suivants :

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Champ Catalogue</b> </th> 
   <th class="entry"> <b>Elément de chaîne dans le champ</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : ImageSet </span> </p> </td> 
   <td> <p>Tout sous-élément contenant une chaîne convertible (délimité par toute combinaison de séparateurs ',' ';' ':' et/ou le début/fin du champ). </p> <p> A <span class="codeph"> 0xrggbb </span> la valeur de couleur au début d’un champ localisable est exclue de la localisation et transmise sans modification. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : Carte </span> </p> </td> 
   <td> <p>Toute valeur d’attribut entre guillemets simples ou doubles, à l’exception des valeurs de la variable <span class="codeph"> coords= </span> et <span class="codeph"> shape= </span> attributs. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue : cibles </span> </p> </td> 
   <td> <p>La valeur de n’importe quel <span class="codeph"> cible.*.label </span> et <span class="codeph"> cible.*.userdata </span> . </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::UserData </span> </p> </td> 
   <td> <p>La valeur de n’importe quelle propriété. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Syntaxe des chaînes {#section-d12320edf300409f8e17565b143acafc}

Activé pour la localisation *`string`* les éléments du catalogue d’images se composent d’une ou de plusieurs chaînes localisées, chacune précédée d’un jeton de localisation.

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
  <td class="stentry"> <p>ID de paramètre régional interne pour la variable <span class="varname"> localizedString </span> à suivre <span class="varname"> localizationToken </span>. </p> </td> 
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

La variable *`locId`* doit être ASCII et ne peut pas inclure &quot;^&quot;.

Le &quot;^&quot; peut se produire n’importe où dans les sous-chaînes avec ou sans codage HTTP. Le serveur correspond à l’intégralité de *`localizationToken`* `^loc=locId^` pour séparer les sous-chaînes.

La variable *`stringElements`*, qui n’incluent pas au moins un *`localizationToken`*, ne sont pas prises en compte pour la localisation.

## La carte des traductions {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` définit les règles utilisées par le serveur pour déterminer laquelle *`localizedStrings`* pour revenir au client. Il se compose d’une liste d’entrées. *`locales`* (correspondant aux valeurs spécifiées avec `locale=`), chacun sans ou plusieurs identifiants de paramètres régionaux internes ( *`locId`*). Par exemple :

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Vide *`locId`* indique que la variable *`defaultString`* doit être renvoyée, le cas échéant.

Reportez-vous à la description de `attribute::LocaleStrMap` pour plus d’informations.

## Processus de traduction {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Compte tenu de l’exemple de carte de traduction ci-dessus et de la requête `/is/image/myCat/myItem?req=&locale=nl`, le serveur commence par rechercher &quot; `nl`&quot; dans la carte des paramètres régionaux. Entrée correspondante `nl,N` indique que pour chaque *`stringElement`*, la variable *`localizedString`* marqué avec `^loc=N^` doit être renvoyée. Si ceci *`localizationToken`* n’est pas présent dans la variable *`stringElement`*, une valeur vide est renvoyée.

Disons `catalog::UserData` pour `myCat/myItem` contient les éléments suivants (sauts de ligne insérés pour plus de clarté) :

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Le serveur renvoie les éléments suivants en réponse à l’exemple de requête :

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Paramètres régionaux inconnus {#section-26dfeefbd60345de94bbfeaaf7741223}

Dans l’exemple ci-dessus, `attribute::LocaleStrMap` comporte une entrée avec une valeur vide *`locale`* . Le serveur utilise cette entrée pour gérer toutes les `locale=` les valeurs qui ne sont pas explicitement spécifiées autrement dans la carte de traduction.

L’exemple de carte de traduction indique que dans ce cas, la variable *`defaultString`* doit être renvoyée, le cas échéant. Par conséquent, le code suivant est renvoyé si ce mappage de traduction est appliqué à la requête . `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Exemples {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Familles de langues**

Multiple *`locId`* peuvent être associées à chaque *`locale`* dans la carte de traduction. Cela est dû au fait qu’il permet la prise en charge de variations spécifiques à un pays ou à une région (par exemple, l’anglais américain ou l’anglais britannique) pour sélectionner *`stringElements`* lors de la gestion de la plupart des contenus avec des paramètres régionaux de base courants (par exemple, l’anglais international).

Dans cet exemple, la prise en charge de l’anglais spécifique aux États-Unis est ajoutée ( `*`locId`* EUS`) et l’anglais spécifique au Royaume-Uni ( `*`locId`* EUK`), pour prendre en charge l’orthographe alternative occasionnelle. Si EUK ou EUS n’existe pas, il revient à E. De même, les variantes allemandes spécifiques à l’Autriche ( `DAT`) peut être rendu disponible si nécessaire tout en renvoyant l’allemand commun. *`localizedStrings`* (marqué par `D`) la plupart du temps.

La variable `attribute::LocaleStrMap` ressemblerait à ceci :

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

Le tableau suivant décrit la sortie de certains composants représentatifs. *`stringElement`* et *`locale`* combinaisons :

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
   <td> <p> <span class="codeph"> ^loc=E^Anglais^loc=D^Allemand </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>Allemand </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^Anglais^loc=UKE^Anglais-UK^loc=D^Allemand^loc=DAT^Autriche </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>UK-English </p> <p>Allemand </p> <p>Autrichien </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^Anglais^loc=USE^US-Anglais^loc=D^Allemand^loc=DDE^Deutsch </span> </p> <p> Dans cet exemple, la variable <span class="varname"> locId </span> Le DDE n’existe pas dans <span class="codeph"> attribute::LocaleStrMap </span>, et donc la sous-chaîne associée à cette opération <span class="varname"> locId </span> n’est jamais renvoyée. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>US-Anglais </p> <p>Allemand </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
