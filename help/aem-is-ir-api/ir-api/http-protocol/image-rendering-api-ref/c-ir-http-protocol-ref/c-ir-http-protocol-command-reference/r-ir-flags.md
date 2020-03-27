---
description: Appliquez des indicateurs. Spécifie des options de rendu supplémentaires.
seo-description: Appliquez des indicateurs. Spécifie des options de rendu supplémentaires.
seo-title: indicateurs
solution: Experience Manager
title: indicateurs
topic: Scene7 Image Serving - Image Rendering API
uuid: 43ed24fe-461e-4973-aa44-8fba66668e6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# indicateurs{#flags}

Appliquez des indicateurs. Spécifie des options de rendu supplémentaires.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Valeur d’indicateur. </p></td> 
 </tr> 
</table>

Actuellement utilisé uniquement pour les matériaux de l&#39;armoire.

`flags=0` (par défaut) rend les armoires supérieures avec des portes solides.

`flags=1` rend les armoires supérieures avec des portes en verre (si la vignette a été créée avec des portes en verre).

## Propriétés {#section-a2b00d7bb15e449ea85178acb92d8285}

Attribut de matière. Ignoré s&#39;il ne s&#39;agit pas d&#39;un matériau d&#39;armoire, ou si l&#39;objet d&#39;armoire  n&#39;autorise pas les portes en verre.

## Par défaut {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` pas de portes en verre.
