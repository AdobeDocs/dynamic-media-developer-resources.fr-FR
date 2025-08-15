---
description: Les valeurs de commande doivent être codées en http à l’aide de séquences d’échappement %xx, de sorte que les chaînes de valeur n’incluent pas les caractères réservés '=', '&' et ' %'.
solution: Experience Manager
title: Encodage HTTP Image Serving
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aec8463f-f72a-4203-89ab-8a4f0ad9d6f9
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 16%

---

# Encodage HTTP Image Serving{#image-serving-http-encoding}

Les valeurs de commande doivent être codées en http à l’aide de séquences d’échappement %xx, de sorte que les chaînes de valeur n’incluent pas les caractères réservés &#39;=&#39;, &#39;&amp;&#39; et &#39; %&#39;.

Dans le cas contraire, les règles de codage HTTP standard s’appliquent. La spécification HTTP exige le codage des caractères non sécurisés, ainsi que des caractères de contrôle, tels que `<return>` et `<tab>`. L’encodage URL d’un caractère se compose d’un symbole « % », suivi de la représentation hexadécimale à deux chiffres (non sensible à la casse) du point de code ISO-latin du caractère. Les caractères et points de code dangereux sont :

<table id="table_D2C01CADB35E477D82D4C27586424625"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Caractère dangereux </th> 
   <th colname="col2" class="entry"> Code points (hexadécimaux) </th> 
   <th colname="col3" class="entry"> Code points (déc) </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Espace </p> </td> 
   <td colname="col2"> <p>20 </p> </td> 
   <td colname="col3"> <p>32 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&lt; </p> </td> 
   <td colname="col2"> <p>3C </p> </td> 
   <td colname="col3"> <p>60 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&gt; </p> </td> 
   <td colname="col2"> <p>3E </p> </td> 
   <td colname="col3"> <p>62 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>" </p> </td> 
   <td colname="col2"> <p>22 </p> </td> 
   <td colname="col3"> <p>34 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p># </p> </td> 
   <td colname="col2"> <p>23 </p> </td> 
   <td colname="col3"> <p>35 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>% </p> </td> 
   <td colname="col2"> <p>25 </p> </td> 
   <td colname="col3"> <p>37 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;lbrace ; </p> </td> 
   <td colname="col2"> <p>7B </p> </td> 
   <td colname="col3"> <p>123 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;rbrace ; </p> </td> 
   <td colname="col2"> <p>7D </p> </td> 
   <td colname="col3"> <p>125 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>| </p> </td> 
   <td colname="col2"> <p>7C </p> </td> 
   <td colname="col3"> <p>124 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>\ </p> </td> 
   <td colname="col2"> <p>5C </p> </td> 
   <td colname="col3"> <p>92 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>^ </p> </td> 
   <td colname="col2"> <p>5E </p> </td> 
   <td colname="col3"> <p>94 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~ </p> </td> 
   <td colname="col2"> <p>7E </p> </td> 
   <td colname="col3"> <p>126 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;lbrack ; </p> </td> 
   <td colname="col2"> <p>5B </p> </td> 
   <td colname="col3"> <p>91 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;rbrack ; </p> </td> 
   <td colname="col2"> <p>5D </p> </td> 
   <td colname="col3"> <p>93 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;grave ; </p> </td> 
   <td colname="col2"> <p>60 </p> </td> 
   <td colname="col3"> <p>96 </p> </td> 
  </tr> 
 </tbody> 
</table>

Les caractères réservés doivent également être encodés.

<table id="table_A6C808A05EA6420F8125186D3D5C9E33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Caractère réservé </th> 
   <th colname="col2" class="entry"> Points Code (hexadécimaux) </th> 
   <th colname="col3" class="entry"> Points Code (déc.) </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>$ </p> </td> 
   <td colname="col2"> <p>24 </p> </td> 
   <td colname="col3"> <p>36 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp; </p> </td> 
   <td colname="col2"> <p>26 </p> </td> 
   <td colname="col3"> <p>38 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>+ </p> </td> 
   <td colname="col2"> <p>2B </p> </td> 
   <td colname="col3"> <p>43 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>, </p> </td> 
   <td colname="col2"> <p>2C </p> </td> 
   <td colname="col3"> <p>44 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>/ </p> </td> 
   <td colname="col2"> <p>2F </p> </td> 
   <td colname="col3"> <p>47 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>: </p> </td> 
   <td colname="col2"> <p>3A </p> </td> 
   <td colname="col3"> <p>58 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>; </p> </td> 
   <td colname="col2"> <p>3B </p> </td> 
   <td colname="col3"> <p>59 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>= </p> </td> 
   <td colname="col2"> <p>3D </p> </td> 
   <td colname="col3"> <p>61 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>? </p> </td> 
   <td colname="col2"> <p>3F </p> </td> 
   <td colname="col3"> <p>63 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>@ </p> </td> 
   <td colname="col2"> <p>40 </p> </td> 
   <td colname="col3"> <p>64 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-b85895e5b6a84b96b7fca987656dd34d}

`…&$text=rate&weight=85% 27#&…`

Si l’obscurcissement n’est pas appliqué, le fragment de requête ci-dessus doit être codé comme suit :

`…&$text=rate%26weight%3D85%25%2027%23&…`

Si l’obscurcissement est appliqué, le codage peut être limité à la suppression des caractères &#39;=&#39;, &#39;&amp;&#39; et &#39; %&#39; :

`…&$text=rate%26weight%3D85%25 27#&…`

## Voir aussi {#section-295476ec34c74973962d07dfa9eb2180}

[Obfuscation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d) de requête, [spécification HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
