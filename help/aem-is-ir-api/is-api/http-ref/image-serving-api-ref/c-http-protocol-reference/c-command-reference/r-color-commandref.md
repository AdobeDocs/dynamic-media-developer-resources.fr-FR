---
description: Couleur de couche. Indique la couleur de premier plan et l’opacité des calques de couleur et d’effet unis, ainsi que la couleur de remplissage de la zone de texte pour les calques de texte.
solution: Experience Manager
title: couleur
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---


# color{#color}

Couleur de couche. Indique la couleur de premier plan et l’opacité des calques de couleur et d’effet unis, ainsi que la couleur de remplissage de la zone de texte pour les calques de texte.

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color  </span> </span> </p> </td> 
  <td class="stentry"> <p>Gris, RVB ou CMJN, avec ou sans alpha. </p> </td> 
 </tr> 
</table>

Dans le cas des calques d’image et de texte, `color=` remplit des zones transparentes et semi-opaques dans le rectangle de délimitation du calque avec la couleur spécifiée* avant* `rotate=` et `extend=` sont appliquées.

## Propriétés {#section-d6e74c36a49547849212e4db8927e678}

Attribut de couche. S&#39;applique au calque actif ou au calque 0 si `layer=comp`.

*`color`* est supposé exister dans l’espace colorimétrique de travail correspondant au type de pixel de  *`color`*. *`color`* est convertie avec précision si l’image de calque a un type de pixel différent au moment de la fusion.

## Par défaut {#section-60611c72876b4c45b5c85ce35608e5ec}

Pas de valeur par défaut pour les calques de couleur et d’effet solides ; une couleur doit être spécifiée. La valeur par défaut est 0,0,0,0 (entièrement transparent) pour les calques d’image et de texte.

## Exemple {#section-2d090493f4ec4e188bbc5565aa151a05}

Dans le fragment de modèle suivant, nous définissons l’arrière-plan du texte avec une couleur opaque à 50 % et utilisons la même couleur pour ajouter une bordure semi-transparente de 10 pixels autour de l’image du calque 2 :

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## Voir aussi {#section-f0e059f857b64b61ab4f23312b8dc619}

[couleur](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5),  [extended=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), bgc=, Gestion des couleurs](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[
