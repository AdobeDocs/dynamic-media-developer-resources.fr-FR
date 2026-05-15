---
description: Valeurs de couleur. Vous pouvez spécifier des valeurs de couleur à l’aide de la notation hexadécimale, d’une liste de valeurs de composant séparées par des virgules ou de décimales.
solution: Experience Manager
title: couleur
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eba88ff0-877d-432e-bbd6-9172f5b460e9
TQID: 'https://experienceleague.adobe.com/3NfMrvwXTP9A-KoxjVPtps-0rhO5xNd04WUlrdCQEo8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 456
ht-degree: 9%

---

# couleur{#color}

Valeurs de couleur. Vous pouvez spécifier des valeurs de couleur à l’aide de la notation hexadécimale, d’une liste de valeurs de composant séparées par des virgules ou de décimales.

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> couleur </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">&amp;lcub;&amp;lcub;<span class="varname"> gris</span>[,<span class="varname"> alpha</span>][g]&amp;rcub;|</span> </p> <p> <span class="codeph"> {<span class="varname"> rouge</span>,<span class="varname"> vert</span>,<span class="varname"> bleu</span>[ ,<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> cyan</span>, <span class="varname"> magenta</span>, <span class="varname"> jaune</span>, <span class="varname"> noir</span>[,alpha]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}&amp;rcub;[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rouge</span>, <span class="varname"> vert</span>, <span class="varname"> bleu</span>, <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>valeur de la composante de couleur (0...255, nombre entier décimal) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cyan</span>, <span class="varname"> magenta</span>, <span class="varname"> jaune</span>, <span class="varname"> noir</span>, <span class="varname"> alpha</span></span> </p></td> 
  <td class="stentry"> <p>Valeur de la composante de couleur CMJN (0..100 %, nombre décimal d’int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> gris</span>, <span class="varname"> alpha</span></span> </p> </td> 
  <td class="stentry"> <p>valeur de la composante de couleur grise (0...100 %, décimale int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>valeur de couleur gris hexadécimal à deux chiffres compressée (GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>gris hexadécimal à quatre chiffres avec une valeur de couleur alpha (GGA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>valeur de couleur RGB hexadécimale à six chiffres compressée (RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>valeur de couleur hexadécimale à huit chiffres RGBA (RRGGBBAA) ou CMJN (CMJN) compactée (si spécifié avec le suffixe 'k') </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>CMJN hexadécimal à dix chiffres avec une valeur alpha (CCYMMKAA) </p> </td> 
 </tr> 
</table>

Les valeurs décimales des composants pour les couleurs RGB sont comprises entre 0 et 255. Les valeurs décimales des composants pour CMJN et gris sont comprises entre 0 et 100 %. Toutes les valeurs des composants hexadécimaux sont comprises entre 0...0xFF.

Les valeurs des composantes de couleur sont supposées être indépendantes de la valeur alpha (non prémultipliées).

Toutes les valeurs de couleur, préfixes et suffixes ne sont pas sensibles à la casse.

Le suffixe de type &#39;k&#39; est requis pour les valeurs de couleur CMJN. Un suffixe de type peut éventuellement être spécifié pour les valeurs de couleur RGB et grise.

Le préfixe &#39;0x&#39; est requis pour les valeurs de couleur grise hexadécimales.

Le suffixe « s » indique que la valeur colorimétrique est associée à l’espace colorimétrique d’entrée (source) correspondant au type de pixel de la valeur colorimétrique (défini avec `attribute::IccProfileSrc*`). Si ce suffixe n’est pas présent, la valeur colorimétrique est associée à l’espace colorimétrique de sortie (de destination) (défini par `icc=` ou `attribute::IccProfile*`).

## Par défaut {#section-737082a7da544acca8092a48d88480e7}

Si une valeur alpha n’est pas spécifiée explicitement, on suppose qu’elle est de 255, 0xFF ou 100 % (opaque complet).

## Exemples {#section-4ac69026349949f8b595a6d4a9ce474d}

Voici quelques exemples de spécificateurs de couleur valides, ainsi que le type de pixel, la valeur de couleur, la valeur alpha et l’espace colorimétrique par défaut correspondants :

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>color</i> </b> </th> 
   <th class="entry"> <b>Type de pixel</b> </th> 
   <th class="entry"> <b>Valeur de couleur</b> </th> 
   <th class="entry"> <b>Valeur </b> </th> 
   <th class="entry"> <b>Espace colorimétrique par défaut </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>RVB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0,100,200,200rs </p> </td> 
   <td> <p>RVB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>200 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0 x 010203 S </p> </td> 
   <td> <p>RVB </p> </td> 
   <td> <p>1,2,3 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>a0b1c2d3R </p> </td> 
   <td> <p>RVB </p> </td> 
   <td> <p>160,177,194 </p> </td> 
   <td> <p>211 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CENTAINES </p> </td> 
   <td> <p>grise </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75 g </p> </td> 
   <td> <p>grise </p> </td> 
   <td> <p>50% </p> </td> 
   <td> <p>75% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>grise </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeegs </p> </td> 
   <td> <p>grise </p> </td> 
   <td> <p>87% </p> </td> 
   <td> <p>93% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94,11,50,33k </p> </td> 
   <td> <p>CMJN </p> </td> 
   <td> <p>94-11-50-33% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26KS </p> </td> 
   <td> <p>CMJN </p> </td> 
   <td> <p>22-23-24-25% </p> </td> 
   <td> <p>26% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMJN </p> </td> 
   <td> <p>56-57-58-59% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0eks </p> </td> 
   <td> <p>CMJN </p> </td> 
   <td> <p>10-11-12-13% </p> </td> 
   <td> <p>14% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

L’espace colorimétrique de sortie spécifié avec `icc=` s’applique au lieu de l’espace colorimétrique par défaut lorsque le type de pixel d’une couleur de sortie correspond au type de pixel de l’image de sortie.
