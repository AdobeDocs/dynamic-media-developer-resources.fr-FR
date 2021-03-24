---
description: Couleur de fond. Indique la couleur de soustraction des textures et des décalcomanies colorables.
solution: Experience Manager
title: bgc
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 6%

---


# bgc{#bgc}

Couleur de fond. Indique la couleur de soustraction des textures et des décalcomanies colorables.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RVB ou valeur de couleur grise. </p></td> 
 </tr> 
</table>

L’algorithme de colorisation de texture de Image Rendering est assez simple : les valeurs de composant de `bgc=` sont soustraites de celles des pixels de texture, `color=` est ajouté et le résultat est ensuite coupé en `0,0,0` et `255,255,255`.

Pour les utilisations courantes de la coloration de texture, la valeur `bgc=` peut être la couleur la plus importante ou la plus dominante dans l’image de texture. Dynamic Media Image Authoring fournit des outils semi-automatiques qui extraient des valeurs de couleur `bgc=` raisonnables des images de textures.

Lorsqu’un matériau de texture est appliqué à un objet de vignette non texturable, `bgc=` est appliqué comme couleur de premier plan si `color=` n’est pas spécifié.

## Propriétés {#section-b2db6f147d7f443ba9f671de04c2ef19}

Attribut de matériau. Ignoré par les matériaux de couleur unie et d&#39;armoire.

## Par défaut {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` si le matériau est basé sur une entrée de catalogue, autrement  `bgc=808080` (gris neutre).

## Exemple {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Coloriser un tissu de vêtements dont la texture a la couleur dominante RVB 120,34,193 :

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Voir aussi {#section-de9958dd63a742b4b5d780c59a57da33}

[catalogue ::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) ,  [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
