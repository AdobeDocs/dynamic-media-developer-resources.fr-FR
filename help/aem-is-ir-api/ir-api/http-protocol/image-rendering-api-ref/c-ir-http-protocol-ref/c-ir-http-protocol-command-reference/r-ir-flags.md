---
title: indicateurs
description: Appliquez des indicateurs. Spécifie les options de rendu supplémentaires.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 5%

---

# indicateurs {#flags}

Appliquez des indicateurs. Spécifie les options de rendu supplémentaires.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Valeur de l’indicateur. </p></td> 
 </tr> 
</table>

Actuellement utilisé uniquement pour les documents de l’armoire.

`flags=0` (par défaut) Rendu des armoires supérieures avec des portes solides.

`flags=1` Rend les armoires supérieures avec des portes en verre (si la vignette a été créée avec des portes en verre).

## Propriétés {#section-a2b00d7bb15e449ea85178acb92d8285}

Attribut de matière. Ignoré s’il ne s’agit pas d’un document de l’armoire ou si l’objet de l’armoire cible n’autorise pas les portes de verre.

## Par défaut {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` Pour pas de portes en verre.
