---
description: Paramètres de rendu avancés. Indique les paramètres de rendu avancés à appliquer lors du rendu de la sélection en cours.
seo-description: Paramètres de rendu avancés. Indique les paramètres de rendu avancés à appliquer lors du rendu de la sélection en cours.
seo-title: rs
solution: Experience Manager
title: rs
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 4ff7fcb4-a10a-4e82-80a1-edf79ae1f717
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---


# rs{#rs}

Paramètres de rendu avancés. Indique les paramètres de rendu avancés à appliquer lors du rendu de la sélection en cours.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Chaîne des paramètres de rendu. </p></td> 
 </tr> 
</table>

Utilisé pour affiner l’aspect du rendu. Utilisez la fonction de rendu de l’outil de création de vignettes (intégré au pack de création d’images Dynamic Media) pour créer des chaînes de paramètres de rendu.

## Propriétés {#section-9a2b2228789046658cb80eddf343af75}

Attribut de matériau.

## Par défaut {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Exemple {#section-47e4811882574441a4d517e42a35f352}

Après une certaine expérimentation dans la création d’images, il est déterminé que le masquage flou (USM) fournit la quantité correcte d’accentuation pour l’application et le matériel donnés. La chaîne des paramètres de rendu qui configure USM est copiée dans la commande `rs=` à utiliser avec ce matériel :

`…&rs=U2V20W50X2&…`

## Voir aussi {#section-930116e735024a008c994547ba36ee40}

[catalogue ::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
