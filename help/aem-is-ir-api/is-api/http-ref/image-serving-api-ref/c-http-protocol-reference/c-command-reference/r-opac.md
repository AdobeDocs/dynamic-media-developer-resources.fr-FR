---
title: opac
description: Ajustez l’opacité de l’image. Permet de réduire l’opacité de premier plan d’une image, d’un texte, d’une couleur unie ou d’un calque d’effet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
TQID: 'https://experienceleague.adobe.com/--AimuhKd3XDT-daEAA73WfUPmCZmaCXSrXmLVO8Y6I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 223
ht-degree: 1%

---

# opac{#opac}

Ajustez l’opacité de l’image. Permet de réduire l’opacité de premier plan d’une image, d’un texte, d’une couleur unie ou d’un calque d’effet.

`opac= *`opacity`*[, *`fillOpacity `*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> opacité</span> </p> </td> 
  <td class="stentry"> <p>Opacité du Principal (0...100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>Opacité du remplissage (0...100 int). </p></td> 
 </tr> 
</table>

L’opacité de premier plan d’un calque d’image est déterminée par le masque de calque ou la couche alpha de l’image, ou, si aucune de ces deux opacités n’est présente, elle est de 100 %. L’opacité de premier plan d’un calque de texte est de 100 % et celle d’un calque de couleur unie est définie par `color=`.

`opac=` ne modifie jamais l’opacité des zones remplies de `color=` ou de `bgColor=`, à l’exception des zones de premier plan des calques de couleur unie et d’effet (définies avec `color=`).

Lorsqu’il est spécifié dans une image, du texte ou un calque de couleur unie, *`opacity`* applique le calque entier, y compris tous les calques d’effet associés, tandis que *`fillOpacity`* s’applique uniquement au contenu du calque principal. Lorsqu’il est spécifié dans un calque d’effet, *`opacity`* s’applique au calque d’effet, tandis que *`fillOpacity`* est ignoré.

L’opacité effective du contenu du calque principal est ( *`opacity`* &#42; *`fillOpacity`* / 100). L&#39;opacité effective pour les calques d&#39;effet est (principale *`opacity`* &#42; effet *`opacity`* / 100).

## Propriétés {#section-ac3f136ff1584a2eab87500b7164f7fa}

Attribut de calque. S’applique au calque actif ou à l’image composite, le cas `layer=comp`.

## Par défaut {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, pour ne pas modifier l’opacité du calque.

## Exemple {#section-9710810e96af40538652e8ae4aadd3be}

... `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`...

Dans cet exemple, l&#39;opacité du texte est de 90&#42;70/100 = 63 % et l&#39;opacité du calque d&#39;effet est de 90&#42;50/100 = 45 %.

## Voir aussi {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
