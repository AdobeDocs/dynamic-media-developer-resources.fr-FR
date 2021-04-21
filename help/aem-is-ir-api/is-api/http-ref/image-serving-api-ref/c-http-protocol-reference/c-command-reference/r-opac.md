---
description: Réglage de l’opacité de l’image. Permet de réduire l’opacité de premier plan d’une image, d’un texte, d’une couleur unie ou d’un calque d’effet.
solution: Experience Manager
title: opac
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 2%

---


# opac{#opac}

Réglage de l’opacité de l’image. Permet de réduire l’opacité de premier plan d’une image, d’un texte, d’une couleur unie ou d’un calque d’effet.

`opac= *``*[, *`opacityfillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> opacité</span> </p> </td> 
  <td class="stentry"> <p>opacité Principal (0...100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>Opacité du remplissage (0...100 int). </p></td> 
 </tr> 
</table>

L’opacité de premier plan d’un calque d’image est déterminée par le masque de calque ou le canal alpha de l’image ou, si aucun des deux n’est présent, elle est de 100 %. L’opacité de premier plan d’un calque de texte est de 100 % et celle d’un calque de couleur unie est définie par `color=`.

`opac=` ne modifie jamais l’opacité des zones remplies de  `color=` ou  `bgColor=`, à l’exception des zones de premier plan des calques de couleur et d’effet solides (définies avec  `color=`).

Lorsqu’elle est spécifiée dans un calque d’image, de texte ou de couleur unie, *`opacity`* applique l’intégralité du calque, y compris tous les calques d’effet associés, tandis que *`fillOpacity`* s’applique uniquement au contenu Principal du calque. Lorsqu&#39;elle est spécifiée dans un calque d&#39;effet, *`opacity`* s&#39;applique au calque d&#39;effet, alors que *`fillOpacity`* est ignoré.

L&#39;opacité effective du contenu du calque principal est ( *`opacity`* * *`fillOpacity`* / 100). L&#39;opacité effective des couches d&#39;effet est (effet principal *`opacity`* * *`opacity`* / 100).

## Propriétés {#section-ac3f136ff1584a2eab87500b7164f7fa}

Attribut de couche. S’applique au calque actif ou à l’image composite si `layer=comp`.

## Par défaut {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, sans modification de l’opacité des calques.

## Exemple {#section-9710810e96af40538652e8ae4aadd3be}

... `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`...

Dans cet exemple, l’opacité du texte est de 90*70/100=63 % et l’opacité du calque d’effets est de 90*50/100=45 %.

## Voir aussi {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
