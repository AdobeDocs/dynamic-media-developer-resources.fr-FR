---
title: Localisation par chaîne de texte
description: La localisation de chaîne de texte permet aux catalogues d’images de contenir plusieurs représentations spécifiques aux paramètres régionaux pour la même valeur de chaîne.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 1%

---

# Localisation par chaîne de texte{#text-string-localization}

La localisation de chaîne de texte permet aux catalogues d’images de contenir plusieurs représentations spécifiques aux paramètres régionaux pour la même valeur de chaîne.

Le serveur renvoie au client la représentation correspondant aux paramètres régionaux spécifiés avec `locale=`, en évitant la localisation côté client et en permettant aux applications de changer de paramètres régionaux simplement en envoyant la valeur appropriée `locale=` avec les requêtes texte IS.

## Portée {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

La localisation par chaîne de texte est appliquée à tous les éléments de chaîne qui incluent le jeton ` ^loc= *`de localisation locId`*^` dans les champs de catalogue suivants :

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Champ Catalogue</b> </th> 
   <th class="entry"> <b>Elément de chaîne dans le champ</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::Visionneuse d’images </span> </p> </td> 
   <td> <p>Tout sous-élément contenant une chaîne traduisible (délimitée par une combinaison quelconque de séparateurs ',' ' ;' ' :' et/ou le début/la fin du champ). </p> <p> Une <span class="codeph"> valeur de couleur 0xrrggbb </span> au début d’un champ localisable est exclue de la localisation et transmise sans modification. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::Carte </span> </p> </td> 
   <td> <p>Toute valeur d’attribut avec guillemet simple ou double, à l’exception des valeurs des <span class="codeph"> attributs coord= </span> et <span class="codeph"> shape= </span> . </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::Cibles </span> </p> </td> 
   <td> <p>Valeur de toute <span class="codeph"> cible.*.label </span> et <span class="codeph"> target.*.userdata </span> . </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::UserData </span> </p> </td> 
   <td> <p>Valeur de toute propriété. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Syntaxe de chaîne {#section-d12320edf300409f8e17565b143acafc}

Les éléments compatibles *`string`* avec la localisation dans le catalogue d’images se composent d’une ou plusieurs chaînes localisées, chacune précédée d’un jeton de localisation.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Elément </span> string </span> </p> </td> 
  <td class="stentry"> <p>[ defaultString <span class="varname">]*{ </span> localizationToken <span class="varname"> </span> localizedString <span class="varname">} </span> </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Jeton </span> de localisation </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>ID de paramètres régionaux interne pour localizedString <span class="varname"> </span> suivant ce <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Chaîne </span> localisée </span> </p> </td> 
  <td class="stentry"> <p>Chaîne localisée. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Chaîne </span> par défaut </span> </p> </td> 
  <td class="stentry"> <p>Chaîne à utiliser pour les paramètres régionaux inconnus. </p> </td> 
 </tr> 
</table>

Ils *`locId`* doivent être ASCII et ne peuvent pas inclure « ^ ».

Le signe « ^ » peut se produire n’importe où dans les sous-chaînes avec ou sans codage HTTP. Le serveur fait correspondre l’ensemble *`localizationToken`* `^loc=locId^` du modèle pour séparer les sous-chaînes.

Les *`stringElements`*, qui n’en incluent pas au moins un *`localizationToken`*, ne sont pas prises en compte pour la localisation.

## La carte de traduction {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` Définit les règles utilisées par le serveur pour déterminer laquelle *`localizedStrings`* renvoyer au client. Il s’agit d’une liste d’entrées *`locales`* (correspondant aux valeurs spécifiées par `locale=`), chacune sans ou plusieurs ID de paramètres régionaux internes ( *`locId`*). Par exemple :

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Les valeurs vides *`locId`* indiquent que la propriété doit être renvoyée, si elle *`defaultString`* est disponible.

Reportez-vous à la description de pour plus de `attribute::LocaleStrMap` détails.

## Le processus de traduction {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Compte tenu de l’exemple de carte de traduction ci-dessus et de la requête `/is/image/myCat/myItem?req=&locale=nl`, le serveur recherche d’abord &quot; `nl`&quot; dans la carte de paramètres régionaux. L’entrée `nl,N` correspondante indique que pour chaque *`stringElement`*, la *`localizedString`* valeur marquée par `^loc=N^` doit être renvoyée. Si la variable *`localizationToken`* *`stringElement`*, une valeur vide est renvoyée.

Disons que `catalog::UserData` pour `myCat/myItem` contient ce qui suit (sauts de ligne insérés pour plus de clarté) :

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Le serveur renverrait ce qui suit en réponse à l’exemple de requête :

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Paramètres régionaux inconnus {#section-26dfeefbd60345de94bbfeaaf7741223}

Dans l’exemple ci-dessus, `attribute::LocaleStrMap` possède une entrée avec une valeur vide *`locale`* . Le serveur utilise cette entrée pour gérer toutes les `locale=` valeurs qui ne sont pas explicitement spécifiées autrement dans la carte de traduction.

L’exemple de carte de traduction spécifie que dans ce cas, la *`defaultString`* propriété doit être renvoyée, si disponible. Par conséquent, le résultat suivant est renvoyé si ce mappage de traduction est appliqué à la requête `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Exemples {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Familles de langues**

Plusieurs *`locId`* valeurs peuvent être associées à chacune *`locale`* dans la carte de traduction. La raison en est qu’il permet de prendre en charge des variations spécifiques à un pays ou à une région (par exemple, l’anglais américain par rapport à l’anglais britannique) pour la sélection *`stringElements`* tout en gérant la plupart des contenus avec des paramètres régionaux de base communs (par exemple, l’anglais international).

Pour l’exemple, la prise en charge est ajoutée pour l’anglais spécifique aux États-Unis ( `*`locId`* EUS`) et l’anglais spécifique au Royaume-Uni ( `*`locId`* EUK`), afin de prendre en charge l’orthographe alternative occasionnelle. Si EUK ou EUS n’existe pas, il revient à E. De même, des variantes allemandes spécifiques à l’Autriche ( `DAT`) pourraient être mises à disposition si nécessaire tout en renvoyant l’allemand *`localizedStrings`* commun (marqué par `D`) la plupart du temps.

Le `attribute::LocaleStrMap` ressemblerait à ceci :

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

Le tableau ci-dessous décrit la sortie pour certaines combinaisons représentatives *`stringElement`* :*`locale`*

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>Elément string</i> </th> 
   <th class="entry"> <i>paramètres régionaux</i> </th> 
   <th class="entry"> <p>Output chaîne </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German </span> </p> </td> 
   <td> <p> fr, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>Tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>Allemand </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> fr, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>Tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>Royaume-Uni-Anglais </p> <p>Allemand </p> <p>Autrichien </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> Pour cet exemple, le DDE locId n’existe <span class="varname"> pas dans </span> attribute ::LocaleStrMap <span class="codeph">et, par conséquent, la sous-chaîne associée à ce </span> locId <span class="varname"> n’est jamais renvoyée.</span> </p> </td> 
   <td> <p> fr, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>Tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>Anglais (États-Unis) </p> <p>Allemand </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
