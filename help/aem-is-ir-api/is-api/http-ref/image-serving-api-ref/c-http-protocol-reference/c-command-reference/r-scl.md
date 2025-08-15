---
title: scl
description: Vue d’échelle. Met à l’échelle l’image composite selon l’inverse de invFactor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# scl{#scl}

Vue d’échelle. Met à l’échelle l’image composite selon l’inverse de invFactor.

`scl= *`Facteur invTarget`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Facteur invTarget</span> </p> </td> 
  <td class="stentry"> <p>Facteur d’échelle inverse (réel supérieur à 0,0). </p></td> 
 </tr> 
</table>

Aucune mise à l’échelle n’est appliquée lorsque `scl=1`. Une *`invFactor`* valeur supérieure à 1.0 down-scales et inférieure à 1.0 agrandit l’image composite.

Si `scl=` est spécifié et `wid=` que et / ou `hei=` sont également présents, l’image est recadrée et/ou `wid=` après la mise à `hei=` l’échelle.

>[!NOTE]
>
>Une erreur est renvoyée si la taille de l’image de réponse calculée ou par défaut est supérieure à `attribute::MaxPix`.

## Propriétés {#section-60af012719db477db4a4703e9a6da5f5}

Afficher l’attribut. Il s’applique quel que soit le paramètre de calque actuel.

## Par défaut {#section-32502fa218a24e1f9c65f41c0260b56a}

Si ni `wid=`, `hei=`ni `scl=` ne sont spécifiés, l’image de réponse a la taille de l’image composite ou `attribute::DefaultPix`, selon la plus petite des deux.

## Exemple {#section-a33f6239476a4b438d939656ad99aa76}

Voir l’exemple dans [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) pour une application courante de `scl=`.

## Voir aussi {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [attribute ::D efaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
