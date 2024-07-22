---
title: bgc
description: Couleur de fond. Spécifie la couleur de substitution des textures et des décalages colorables.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# bgc {#bgc}

Couleur de fond. Spécifie la couleur de substitution des textures et des décalages colorables.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>Valeur de couleur RGB ou grise. </p></td> 
 </tr> 
</table>

L’algorithme de colorisation de texture du rendu d’image est simple : les valeurs des composants de `bgc=` sont soustraites des valeurs des pixels de texture ; `color=` est ajouté et, enfin, le résultat est tronqué à `0,0,0` et `255,255,255`.

Pour les utilisations courantes de la colorisation de texture, la valeur de `bgc=` peut être la couleur la plus importante ou la plus dominante dans l’image de texture. La création d’images Dynamic Media fournit des outils semi-automatiques qui extraient des valeurs de couleur `bgc=` raisonnables des images de textures.

Lorsqu’un matériau de texture est appliqué à un objet de vignette non texturable, `bgc=` est appliqué comme couleur de premier plan si `color=` n’est pas spécifié.

## Propriétés {#section-b2db6f147d7f443ba9f671de04c2ef19}

Attribut de matière. Ignoré par les matériaux de couleur et d’armoire solides.

## Par défaut {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` Si la matière est basée sur une entrée de catalogue, sinon `bgc=808080` (gris neutre).

## Exemple {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Coloriez un tissu de vêtements dont la texture a la couleur dominante du RGB 120,34,193 :

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Voir aussi {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
