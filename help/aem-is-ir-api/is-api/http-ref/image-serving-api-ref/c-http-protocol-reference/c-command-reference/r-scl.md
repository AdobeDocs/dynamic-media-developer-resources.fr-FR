---
description: Vue Échelle. Met à l’échelle l’image composite par l’inverse de l’attribut d’événement d’événement.
solution: Experience Manager
title: scl
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---

# scl{#scl}

Vue Échelle. Met à l’échelle l’image composite par l’inverse de l’attribut d’événement d’événement.

`scl= *`Factor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Factor</span> </p> </td> 
  <td class="stentry"> <p>Facteur d’échelle inversé (réel supérieur à 0,0). </p></td> 
 </tr> 
</table>

Aucune mise à l’échelle n’est appliquée lorsque `scl=1`. *`invFactor`* plus grande que 1,0, plus petite que 1,0 agrandit l’image composite.

Si `scl=` est spécifié et que `wid=` et/ou `hei=` sont également présents, l’image est recadrée sur `wid=` et/ou `hei=` après la mise à l’échelle.

>[!NOTE]
>
>Une erreur est renvoyée si la taille de l’image de réponse calculée ou par défaut est supérieure à `attribute::MaxPix`.

## Propriétés {#section-60af012719db477db4a4703e9a6da5f5}

Afficher l’attribut. S’applique quel que soit le paramètre de calque actif.

## Par défaut {#section-32502fa218a24e1f9c65f41c0260b56a}

Si aucun `wid=`, `hei=` ou `scl=` n’est spécifié, l’image de réponse aura la taille de l’image composite ou `attribute::DefaultPix`, selon la valeur la plus petite.

## Exemple {#section-a33f6239476a4b438d939656ad99aa76}

Voir l’exemple dans [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) pour une application commune de `scl=`.

## Voir aussi {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
