---
title: indicateurs
description: Appliquer des indicateurs. Spécifie les options de rendu supplémentaires.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
TQID: 'https://experienceleague.adobe.com/tdbtQIxutlPSPRm4vGWCQLM8veyivWfabKos9YbvfYg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 4%

---

# indicateurs {#flags}

Appliquer des indicateurs. Spécifie les options de rendu supplémentaires.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Valeur de l’indicateur . </p></td> 
 </tr> 
</table>

Actuellement utilisé uniquement pour les matériaux d’armoire.

`flags=0` (par défaut) Rend les armoires supérieures avec des portes pleines.

`flags=1` Rend les armoires supérieures avec des portes vitrées (si la vignette a été créée avec des portes vitrées).

## Propriétés {#section-a2b00d7bb15e449ea85178acb92d8285}

Attribut Material. Ignoré s&#39;il ne s&#39;agit pas d&#39;un matériau d&#39;armoire ou si l&#39;objet d&#39;armoire cible n&#39;autorise pas les portes vitrées.

## Par défaut {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` Pour pas de portes vitrées.

