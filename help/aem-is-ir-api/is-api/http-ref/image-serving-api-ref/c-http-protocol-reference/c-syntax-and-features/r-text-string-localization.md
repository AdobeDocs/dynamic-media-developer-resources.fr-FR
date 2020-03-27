---
description: Le de chaînes de texte permet aux catalogues d’images de contenir plusieurs représentations spécifiques aux paramètres régionaux pour la même valeur de chaîne.
seo-description: Le de chaînes de texte permet aux catalogues d’images de contenir plusieurs représentations spécifiques aux paramètres régionaux pour la même valeur de chaîne.
seo-title: ' de chaîne de texte'
solution: Experience Manager
title: ' de chaîne de texte'
topic: Scene7 Image Serving - Image Rendering API
uuid: bdff2403-e3bb-4b3f-a8d7-bb108c1fbee8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


#  de chaîne de texte{#text-string-localization}

Le de chaînes de texte permet aux catalogues d’images de contenir plusieurs représentations spécifiques aux paramètres régionaux pour la même valeur de chaîne.

Le serveur renvoie au client la représentation correspondant aux paramètres régionaux spécifiés par `locale=`, évitant ainsi les  côté client et permettant aux applications de changer de paramètres régionaux simplement en envoyant la `locale=` valeur appropriée avec les requêtes de texte IS.

## Etendue {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

Le de chaîne de texte est appliqué à tous les éléments de chaîne qui incluent le jeton de  de ` ^loc= *`locId`*^` dans les champs de catalogue suivants :

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Champ Catalogue</b> </th> 
   <th class="entry"> <b>Elément de chaîne dans le champ</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue::ImageSet </span> </p> </td> 
   <td> <p>Tout sous-élément contenant une chaîne convertible (délimité par une combinaison quelconque de séparateurs ',' ';' ':' et/ou le /la fin du champ). </p> <p> Une valeur de <span class="codeph"> couleur </span> 0xrrggbb au début d’un champ localisable est exclue du  et transmise sans modification. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue ::Carte </span> </p> </td> 
   <td> <p>Toute valeur d’attribut entre guillemets simples ou, à l’exception des valeurs des attributs <span class="codeph"> coords= </span> et <span class="codeph"> shape= </span> . </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue :: </span> </p> </td> 
   <td> <p>Valeur de tout <span class="codeph"> .*.label </span> et <span class="codeph"> .*.userdata, </span> propriété. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogue::UserData </span> </p> </td> 
   <td> <p>Valeur d’une propriété. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Syntaxe de chaîne {#section-d12320edf300409f8e17565b143acafc}

Les *`string`* éléments activés pour les  dans le catalogue d’images se composent d’une ou de plusieurs chaînes localisées, chacune étant précédée d’un jeton .

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span></span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> localizedString <span class="varname"> </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span></span> </p> </td> 
  <td class="stentry"> <p>ID de paramètre régional interne pour la <span class="varname"> chaîne localisée </span> qui suit ce <span class="varname"> jeton de localisation </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span></span> </p> </td> 
  <td class="stentry"> <p>Chaîne localisée. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span></span> </p> </td> 
  <td class="stentry"> <p>Chaîne à utiliser pour les paramètres régionaux inconnus. </p> </td> 
 </tr> 
</table>

*`locId`* doit être ASCII et ne peut pas inclure &quot;^&quot;.

&#39;^&#39; peut se produire n’importe où dans les sous-chaînes avec ou sans encodage HTTP. Le serveur fait correspondre l’ensemble du *`localizationToken`* modèle `^loc=locId^` à des sous-chaînes distinctes.

*`stringElements`* qui n&#39;incluent pas au moins un n&#39; *`localizationToken`* est pas pris en compte pour les  de.

## La carte de la traduction {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` définit les règles utilisées par le serveur pour déterminer le *`localizedStrings`* retour au client. Il se compose d’un d’entrée *`locales`* (correspondant aux valeurs spécifiées par `locale=`), chacun avec aucun ou plusieurs identifiants de paramètres régionaux internes ( *`locId`*). Par exemple :

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Les *`locId`* valeurs vides indiquent que le *`defaultString`* paramètre doit être renvoyé, le cas échéant.

Consultez la description de `attribute::LocaleStrMap` pour plus de détails.

## Le processus de traduction {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Compte tenu de l’exemple de mappage de traduction ci-dessus et de la requête `/is/image/myCat/myItem?req=&locale=nl`, le serveur commence par rechercher &quot; `nl`&quot; dans le mappage de paramètres régionaux. L’entrée correspondante `nl,N` indique que pour chaque *`stringElement`*, la *`localizedString`* marque `^loc=N^` doit être renvoyée. S’il *`localizationToken`* n’est pas présent dans la *`stringElement`*, une valeur vide est renvoyée.

Supposons que `catalog::UserData` contient `myCat/myItem` les éléments suivants (sauts de ligne insérés pour plus de clarté) :

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Le serveur renverra ce qui suit en réponse à notre exemple de requête :

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Paramètres régionaux inconnus {#section-26dfeefbd60345de94bbfeaaf7741223}

Dans l’exemple ci-dessus, `attribute::LocaleStrMap` comporte une entrée avec une *`locale`* valeur vide. Le serveur utilise cette entrée pour gérer toutes les `locale=` valeurs qui ne sont pas explicitement spécifiées autrement dans le mappage de traduction.

L’exemple de mappage de traduction indique que dans un tel cas, le *`defaultString`* texte doit être renvoyé s’il est disponible. Ainsi, les éléments suivants seraient renvoyés si cette carte de traduction était appliquée à la requête `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Exemples {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Familles de langues**

Plusieurs *`locId`* valeurs peuvent être associées à chacune *`locale`* dans la carte de traduction. Cela permet de prendre en charge les variations spécifiques à un pays ou à une région (par exemple, Anglais américain ou Anglais britannique) pour le choix *`stringElements`* tout en gérant la plupart des contenus avec des paramètres régionaux de base communs (par exemple, Anglais international).

Pour notre exemple, nous souhaitons ajouter la prise en charge de l’anglais spécifique aux Etats-Unis ( ` *`locId`* EUS`) et de l’anglais spécifique au Royaume-Uni ( ` *`locId`* EUK`), afin de prendre en charge l’orthographe alternative occasionnelle. Si EUK ou EUS n&#39;existent pas, nous retomberions sur E. De même, des variantes allemandes spécifiques à l&#39;Autriche ( `DAT`) pouvaient être rendues disponibles lorsque cela était nécessaire tout en retournant l&#39;allemand commun *`localizedStrings`* (marqué par `D`) la plupart du temps.

`attribute::LocaleStrMap` ressemblerait à ceci :

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

Le tableau suivant décrit la sortie pour certaines combinaisons représentatives *`stringElement`* et *`locale`* combinaisons :

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^Allemand^loc=DAT^Autrichien </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>Anglais-Royaume-Uni </p> <p>Allemand </p> <p>Autrichien </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^Anglais^loc=USE^US-Anglais^loc=D^Allemand^loc=DDE^Deutsch </span> </p> <p> Notez que pour cet exemple, le <span class="varname"> DDE locId </span> n’existe pas dans <span class="codeph"> attribut::LocaleStrMap </span>, et donc la sous-chaîne associée à ce <span class="varname"> locId </span> n’est jamais renvoyée. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>tous les autres </p> </td> 
   <td> <p>Anglais </p> <p>Anglais américain </p> <p>Allemand </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

