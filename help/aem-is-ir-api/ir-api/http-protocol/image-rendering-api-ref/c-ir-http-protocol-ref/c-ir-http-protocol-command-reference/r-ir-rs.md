---
description: Paramètres de rendu avancés. Spécifie des paramètres de rendu avancés à appliquer lors du rendu de la sélection en cours.
solution: Experience Manager
title: rs
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# rs{#rs}

Paramètres de rendu avancés. Spécifie des paramètres de rendu avancés à appliquer lors du rendu de la sélection en cours.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Chaîne des paramètres de rendu. </p></td> 
 </tr> 
</table>

Utilisé pour affiner l’aspect du rendu. Utilisez la fonction de rendu de l’outil de création de vignettes (qui fait partie du package Dynamic Media Image Authoring) pour créer des chaînes de paramètres de rendu.

## Propriétés {#section-9a2b2228789046658cb80eddf343af75}

Attribut de matière.

## Par défaut {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Exemple {#section-47e4811882574441a4d517e42a35f352}

Après une certaine expérience dans la création d’images, il est déterminé que le masquage flou (USM) fournit la bonne quantité d’accentuation pour l’application et le matériel donnés. La chaîne des paramètres de rendu qui configure USM est copiée dans la commande `rs=` à utiliser avec ce matériel :

`…&rs=U2V20W50X2&…`

## Voir aussi {#section-930116e735024a008c994547ba36ee40}

[catalogue ::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
