---
title: scl
description: Mode Échelle. Met à l’échelle l’image composite de l’inverse de invFactor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
TQID: 'https://experienceleague.adobe.com/Evu9NXhBJE-Z4inLuaWJkiJikd2yslhec5q7C2azxKw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 2%

---

# scl{#scl}

Mode Échelle. Met à l’échelle l’image composite de l’inverse de invFactor.

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>Facteur d'échelle inverse (réel supérieur à 0,0). </p></td> 
 </tr> 
</table>

Aucune mise à l’échelle n’est appliquée lors de la `scl=1`. Une valeur *`invFactor`* supérieure à 1,0 réduit et inférieure à 1,0 agrandit l’image composite.

Si `scl=` est spécifié et que des `wid=` et/ou des `hei=` sont également présents, l’image est recadrée en `wid=` et/ou `hei=` après mise à l’échelle.

>[!NOTE]
>
>Une erreur est renvoyée si la taille de l’image de réponse calculée ou par défaut est supérieure à `attribute::MaxPix`.

## Propriétés {#section-60af012719db477db4a4703e9a6da5f5}

Attribut d’affichage. Il s’applique quel que soit le paramètre de calque actif.

## Par défaut {#section-32502fa218a24e1f9c65f41c0260b56a}

Si ni `wid=`, `hei=` ou `scl=` n’est spécifié, l’image de réponse a la taille de l’image composite ou de la `attribute::DefaultPix`, la plus petite des deux.

## Exemple {#section-a33f6239476a4b438d939656ad99aa76}

Voir l’exemple dans [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) pour une application courante de `scl=`.

## Voir aussi {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
