---
description: Les valeurs de commande doivent être codées au format http à l’aide des séquences d’échappement %xx, de sorte que les chaînes de valeur n’incluent pas les caractères réservés '=', '&' et '%'.
seo-description: Les valeurs de commande doivent être codées au format http à l’aide des séquences d’échappement %xx, de sorte que les chaînes de valeur n’incluent pas les caractères réservés '=', '&' et '%'.
seo-title: Codage HTTP Image Serving
solution: Experience Manager
title: Codage HTTP Image Serving
topic: Scene7 Image Serving - Image Rendering API
uuid: e7fb368b-060a-439e-95a1-16b94d4796dc
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# Codage HTTP Image Serving{#image-serving-http-encoding}

Les valeurs de commande doivent être codées au format http à l’aide des séquences d’échappement %xx, de sorte que les chaînes de valeur n’incluent pas les caractères réservés &#39;=&#39;, &#39;&amp;&#39; et &#39;%&#39;.

Sinon, les règles de codage HTTP standard s’appliquent. La spécification HTTP requiert le codage des caractères dangereux, ainsi que des caractères de contrôle, tels que `<return>` et `<tab>`. Le codage d’URL d’un caractère est constitué d’un symbole &quot;%&quot;, suivi de la représentation hexadécimale à deux chiffres (non-respect de la casse) du point de code ISO-Latin du caractère. Les caractères et les points de code dangereux sont les suivants :

<table id="table_D2C01CADB35E477D82D4C27586424625"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Caractère non sécurisé </th> 
   <th colname="col2" class="entry"> Points de code (hex) </th> 
   <th colname="col3" class="entry"> Points de code (dec) </th> 
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
   <td colname="col1"> <p>{ </p> </td> 
   <td colname="col2"> <p>7B </p> </td> 
   <td colname="col3"> <p>123 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>} </p> </td> 
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
   <td colname="col1"> <p>[ </p> </td> 
   <td colname="col2"> <p>5B </p> </td> 
   <td colname="col3"> <p>91 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>] </p> </td> 
   <td colname="col2"> <p>5D </p> </td> 
   <td colname="col3"> <p>93 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>` </p> </td> 
   <td colname="col2"> <p>60 </p> </td> 
   <td colname="col3"> <p>96 </p> </td> 
  </tr> 
 </tbody> 
</table>

Les caractères réservés doivent également être codés.

<table id="table_A6C808A05EA6420F8125186D3D5C9E33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Caractère réservé </th> 
   <th colname="col2" class="entry"> Points de code (hexadécimal) </th> 
   <th colname="col3" class="entry"> Points de code (décembre) </th> 
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

Si l’obscurcissement est appliqué, le codage peut être limité à la suppression des caractères &#39;=&#39;, &#39;&amp;&#39; et &#39;%&#39; :

`…&$text=rate%26weight%3D85%25 27#&…`

## Voir aussi {#section-295476ec34c74973962d07dfa9eb2180}

[Obscurcissement](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)de requête, Spécification [HTTP/1.1 (RFC 2616)](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
