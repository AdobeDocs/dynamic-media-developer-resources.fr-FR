---
description: Valeurs de couleur. Vous pouvez spécifier des valeurs de couleur à l’aide d’une notation hexadécimale, d’une liste de valeurs de composant séparées par des virgules ou de décimales.
solution: Experience Manager
title: couleur
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 14%

---


# color{#color}

Valeurs de couleur. Vous pouvez spécifier des valeurs de couleur à l’aide d’une notation hexadécimale, d’une liste de valeurs de composant séparées par des virgules ou de décimales.

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">{{<span class="varname"> gray</span>[,<span class="varname"> alpha</span>][g]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> rouge</span>,<span class="varname"> vert</span>,<span class="varname"> bleu</span>[,<span class="varname"> rgbAlpha][r]}|</span></span> </p> <p> <span class="codeph"> {<span class="varname"> cyan</span>,  <span class="varname"> magenta</span>,  <span class="varname"> jaune</span>,  <span class="varname"> noir[,alpha]k}|</span></span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}}[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rouge</span>,  <span class="varname"> vert</span>,  <span class="varname"> bleu</span>,  <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>valeur du composant de couleur (0...255, décimal int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cyan</span>,  <span class="varname"> magenta</span>,  <span class="varname"> jaune</span>,  <span class="varname"> noir</span>, alpha</span></span><span class="varname"> </span></p></td> 
  <td class="stentry"> <p>Valeur de la composante de couleur CMJN (0,100 %, décimal int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> gris</span>,  <span class="varname"> alpha</span></span> </p> </td> 
  <td class="stentry"> <p>valeur de la composante de couleur grise (0...100 %, décimal int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>valeur de couleur grise hexadécimale à deux chiffres (GG) compressée </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>compressé à quatre chiffres hex gray avec une valeur de couleur alpha (GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>valeur de couleur RVB hexadécimale à six chiffres (RRGBB) compressée </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>valeur de couleur hexadécimale RGBA (RRGBBAA) ou CMJN (CCMYYKK) à huit chiffres (si spécifiée avec le suffixe k) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>CMJN hexadécimal à dix chiffres avec valeur alpha (CCYMMKAA) </p> </td> 
 </tr> 
</table>

Les valeurs des composants décimaux des couleurs RVB sont comprises dans la plage 0...255. Les valeurs des composants décimaux pour CMJN et gris sont comprises dans la plage de 0,100 %. Toutes les valeurs de composants hexadécimaux sont comprises dans la plage 0...0xFF.

Les valeurs des composantes de couleur sont supposées être indépendantes de la valeur alpha (non prémultipliées).

Toutes les valeurs de couleur, préfixes et suffixes ne sont pas sensibles à la casse.

Le suffixe de type &#39;k&#39; est requis pour les valeurs de couleur CMJN. Un suffixe de type peut éventuellement être spécifié pour les valeurs RVB et de couleur grise.

Le préfixe 0x est requis pour les valeurs de couleur grise hexadécimales.

Le suffixe &#39;s&#39; spécifie que la valeur de couleur est associée à l&#39;espace colorimétrique d&#39;entrée (source) correspondant au type de pixel de la valeur de couleur (défini par `attribute::IccProfileSrc*`). Si ce suffixe n’est pas présent, la valeur de couleur est associée à l’espace colorimétrique de sortie (destination) (défini par `icc=` ou `attribute::IccProfile*`).

## Par défaut {#section-737082a7da544acca8092a48d88480e7}

Si aucune valeur alpha n’est explicitement spécifiée, elle est supposée être de 255, 0xFF ou de 100 % (entièrement opaque).

## Exemples {#section-4ac69026349949f8b595a6d4a9ce474d}

Voici quelques exemples de paramètres de couleurs valides, ainsi que le type de pixel, la valeur de couleur, la valeur alpha et l’espace colorimétrique par défaut correspondants :

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>color</i> </b> </th> 
   <th class="entry"> <b>Type de pixel</b> </th> 
   <th class="entry"> <b>Valeur de couleur</b> </th> 
   <th class="entry"> <b>Valeur Alpha</b> </th> 
   <th class="entry"> <b>Espace colorimétrique par défaut  </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0 100 200 </p> </td> 
   <td> <p>RVB </p> </td> 
   <td> <p>0 100 200 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0 100 200 200 rs </p> </td> 
   <td> <p>RVB </p> </td> 
   <td> <p>0 100 200 </p> </td> 
   <td> <p>200 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x010203S </p> </td> 
   <td> <p>RVB </p> </td> 
   <td> <p>1,2,3 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>a0b1c2d3R </p> </td> 
   <td> <p>RVB </p> </td> 
   <td> <p>160 177 194 </p> </td> 
   <td> <p>211 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>100 S </p> </td> 
   <td> <p>gris </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75g </p> </td> 
   <td> <p>gris </p> </td> 
   <td> <p>50 % </p> </td> 
   <td> <p>75% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>gris </p> </td> 
   <td> <p>44 % </p> </td> 
   <td> <p>44 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeegs </p> </td> 
   <td> <p>gris </p> </td> 
   <td> <p>87 % </p> </td> 
   <td> <p>93 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94,11,50,33 ko </p> </td> 
   <td> <p>CMJN </p> </td> 
   <td> <p>94-11-50-33 % </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26 KS </p> </td> 
   <td> <p>CMJN </p> </td> 
   <td> <p>22-23-24-25 % </p> </td> 
   <td> <p>26% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMJN </p> </td> 
   <td> <p>56-57-58-59 % </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0eks </p> </td> 
   <td> <p>CMJN </p> </td> 
   <td> <p>10-11-12-13 % </p> </td> 
   <td> <p>14 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

L’espace colorimétrique de sortie spécifié avec `icc=` s’applique à la place de l’espace colorimétrique par défaut lorsque le type de pixel d’une couleur de sortie correspond au type de pixel de l’image de sortie.
