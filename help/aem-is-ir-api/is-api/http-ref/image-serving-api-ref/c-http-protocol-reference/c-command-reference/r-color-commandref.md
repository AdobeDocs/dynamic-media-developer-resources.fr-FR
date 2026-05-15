---
title: couleur
description: Couleur du calque. Indique la couleur de premier plan et l’opacité des calques de couleur unie et d’effet, ainsi que la couleur de remplissage de la zone de texte pour les calques de texte.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
TQID: 'https://experienceleague.adobe.com/tjiZfVTztBPgsIYS1SGtVeBxo0Wq1q8Ur-kq3Xtm6og'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 202
ht-degree: 3%

---

# couleur{#color}

Couleur du calque. Indique la couleur de premier plan et l’opacité des calques de couleur unie et d’effet, ainsi que la couleur de remplissage de la zone de texte pour les calques de texte.

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> couleur </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur de couleur grise, RGB ou CMJN, avec ou sans couche alpha. </p> </td> 
 </tr> 
</table>

S’il existe des calques d’image et de texte, `color=` remplit les zones transparentes et semi-opaques dans le rectangle de délimitation du calque avec la couleur spécifiée* avant* l’application des `rotate=` et `extend=`.

## Propriétés {#section-d6e74c36a49547849212e4db8927e678}

Attribut de calque. S’applique au calque actuel ou au calque 0, le cas `layer=comp`.

Le modificateur *`color`* est supposé exister dans l’espace colorimétrique de travail correspondant au type de pixel de l’*`color`*. Et *`color`* est converti avec précision si l’image du calque a un type de pixel différent au moment de la fusion.

## Par défaut {#section-60611c72876b4c45b5c85ce35608e5ec}

Aucune valeur par défaut pour les calques de couleur unie et d&#39;effet ; une couleur doit être spécifiée. La valeur par défaut est 0,0,0,0 (entièrement transparent) pour les calques d’image et de texte.

## Exemple {#section-2d090493f4ec4e188bbc5565aa151a05}

Dans le fragment de modèle suivant, l’arrière-plan du texte est défini sur une couleur opaque à 50 % et utilise la même couleur pour ajouter une bordure semi-transparente de 10 pixels autour de l’image du calque 2 :

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## Voir aussi {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
