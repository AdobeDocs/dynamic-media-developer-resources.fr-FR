---
title: origine
description: Origine du calque.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
TQID: 'https://experienceleague.adobe.com/-wkJjmR-LwxC90IMLNXldXSiaugkaYRyvLS17-nbJAM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 165
ht-degree: 2%

---

# origine{#origin}

Origine du calque.

`origin= *`coord`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p></td> 
  <td class="stentry"> <p>Décalage en pixels à partir du coin supérieur gauche du calque rect (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Décalage normalisé par rapport au centre du calque rect (réel, réel). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>Le calque rect inclut toujours toute modification par `extend=`.

Définit le point d’alignement du rectangle de calque, qui est utilisé pour positionner le rectangle de calque par rapport au calque 0 par `pos=`. `originN=0,0` positionne l&#39;origine du calque au centre du rectangle du calque. `originN=-0.5,-0.5` et `origin=0,0` est le coin supérieur gauche et `originN=0.5,0.5` est le coin inférieur droit du rectangle du calque.

## Propriétés {#section-60f639e36ada43d1abc6bfc100afc925}

Attribut de calque. S’applique au calque actif ou au calque 0, le cas `layer=comp`. Non affecté par les transformations de calque ( `crop=`, `scale=`, `rotate=`, `flip=`) appliquées à la source de calque. Remplace `anchor=`. Ignoré par les calques d’effet.

## Par défaut {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

Si `origin=` n’est pas spécifié, l’origine du calque est déterminée en appliquant les transformations de calque à l’ancre d’image. Si l’ancre d’image n’est pas connue, le centre du rectangle du calque ( `originN=0,0`) est utilisé.

## Exemple {#section-13e38d6e17be4e6cbc6b27fbde63b291}

Voir Exemple A dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
