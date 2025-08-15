---
title: opac
description: Modifie l’opacité de l’image. Permet de réduire l’opacité de premier plan d’une image, d’un texte, d’une couleur unie ou d’un calque d’effets.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# opac{#opac}

Modifie l’opacité de l’image. Permet de réduire l’opacité de premier plan d’une image, d’un texte, d’une couleur unie ou d’un calque d’effets.

`opac= *`opacité`*[, *`fillopacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> opacité</span> </p> </td> 
  <td class="stentry"> <p>Opacité primaire (0... 100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Opacité du remplissage</span> </p></td> 
  <td class="stentry"> <p>Opacité de remplissage (0... 100 int). </p></td> 
 </tr> 
</table>

L’opacité de premier plan d’un calque d’image est déterminée par le masque de calque ou le canal alpha de l’image ou, si aucun des deux n’est présent, elle est de 100 %. L’opacité de premier plan d’un calque de texte est de 100 % et celle d’un calque de couleur unie est définie par `color=`.

`opac=` ne modifie jamais l’opacité des zones remplies de `color=` ou `bgColor=`, à l’exception des zones de premier plan de calques de couleur unie et d’effet (définie avec `color=`).

Lorsqu’il est spécifié dans une image, un texte ou un calque de couleur unie, *`opacity`* applique l’intégralité du calque, y compris tous les calques d’effets associés, tandis que *`fillOpacity`* s’applique uniquement au contenu du calque principal. Lorsqu’il est spécifié dans un calque d’effets, *`opacity`* s’applique au calque d’effet, alors que *`fillOpacity`* est ignoré.

L’opacité effective pour le contenu du calque principal est ( *`opacity`* &#42; *`fillOpacity`* / 100). L’opacité effective pour les calques d’effets est (effet *`opacity`* principal &#42; *`opacity`* / 100).

## Propriétés {#section-ac3f136ff1584a2eab87500b7164f7fa}

Attribut de calque. S’applique au calque actif ou à l’image composite si `layer=comp`.

## Par défaut {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, sans modification de l’opacité du calque.

## Exemple {#section-9710810e96af40538652e8ae4aadd3be}

... `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

L’opacité du texte dans cet exemple est 90&#42;70/100=63 %, et l’opacité du calque d’effet est 90&#42;50/100=45 %.

## Voir aussi {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
