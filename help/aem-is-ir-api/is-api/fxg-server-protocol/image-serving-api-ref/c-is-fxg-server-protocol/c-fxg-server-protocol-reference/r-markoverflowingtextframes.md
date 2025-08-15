---
description: Affichez les blocs de texte en excès avec le signe plus. Un indicateur de dépassement de texte indique quand le texte dépasse l’espace qui lui est alloué dans un bloc de texte (ou dans le dernier bloc de texte dans le cas du texte fileté). Cet indicateur est représenté sous la forme d’un cadre rouge avec un signe plus.
solution: Experience Manager
title: MarkOverflowingTextFrames
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1e2a3d4-ef1f-4d5e-be9c-eeec36f46603
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---

# MarkOverflowingTextFrames{#markoverflowingtextframes}

Affichez les blocs de texte en excès avec le signe plus. Un indicateur de dépassement de texte indique quand le texte dépasse l’espace qui lui est alloué dans un bloc de texte (ou dans le dernier bloc de texte dans le cas du texte fileté). Cet indicateur est représenté sous la forme d’un cadre rouge avec un signe plus.

<table id="simpletable_F17FD29EB52043BF9000923ED5195A26"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;markOverflowingTextFrames</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

La définition du modificateur `markOverflowingTextFrames=1` via un appel d’URL marque tous les blocs de texte où le texte est surchargé d’un signe plus. En outre, dans Dynamic Media aperçu Classic, l’indicateur de texte en excès est défini sur &quot; `TRUE`&quot; par défaut.

Par défaut : 0.
