---
description: Affichez des cadres de texte superposés avec le signe plus. Un indicateur de débordement de texte s’affiche lorsque le texte dépasse l’espace qui lui est alloué dans un cadre de texte (ou dans la dernière zone de texte dans le cas d’un texte en thread). L’indicateur est une zone rouge contenant un signe plus.
solution: Experience Manager
title: markOverflowTextFrames
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1e2a3d4-ef1f-4d5e-be9c-eeec36f46603
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---

# markOverflowTextFrames{#markoverflowingtextframes}

Affichez des cadres de texte superposés avec le signe plus. Un indicateur de débordement de texte s’affiche lorsque le texte dépasse l’espace qui lui est alloué dans un cadre de texte (ou dans la dernière zone de texte dans le cas d’un texte en thread). L’indicateur est une zone rouge contenant un signe plus.

<table id="simpletable_F17FD29EB52043BF9000923ED5195A26"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;markOverflowTextFrames</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

La définition du modificateur `markOverflowingTextFrames=1` par le biais d’un appel URL marque tous les cadres de texte dans lesquels le texte est surchargé avec un signe plus. En outre, dans le prévisualiseur Dynamic Media Classic, l’indicateur de remplacement de texte est défini sur &quot; `TRUE`&quot; par défaut.

Par défaut : 0.
