---
title: RS
description: Paramètres de rendu avancés. Spécifie les paramètres de rendu avancés à appliquer lors du rendu de la sélection actuelle.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# RS{#rs}

Paramètres de rendu avancés. Spécifie les paramètres de rendu avancés à appliquer lors du rendu de la sélection actuelle.

`rs= *`Val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Val</span> </p> </td> 
  <td class="stentry"> <p>Chaîne de paramètres de rendu. </p></td> 
 </tr> 
</table>

Utilisé pour affiner l’aspect du rendu. Pour créer des chaînes de paramètres de rendu, utilisez la fonctionnalité de rendu de l’outil de création de vignettes (qui fait partie du package Dynamic Media Image Authoring).

## Propriétés {#section-9a2b2228789046658cb80eddf343af75}

Attribut matériel.

## Par défaut {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Exemple {#section-47e4811882574441a4d517e42a35f352}

Après quelques expériences dans Image Authoring, il est déterminé que le masquage flou (USM) fournit la quantité correcte d’accentuation pour l’application et le matériau donnés. La chaîne de paramètres de rendu qui configure USM est copiée dans la `rs=` commande à utiliser avec ce matériau :

`…&rs=U2V20W50X2&…`

## Voir aussi {#section-930116e735024a008c994547ba36ee40}

[catalog ::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
