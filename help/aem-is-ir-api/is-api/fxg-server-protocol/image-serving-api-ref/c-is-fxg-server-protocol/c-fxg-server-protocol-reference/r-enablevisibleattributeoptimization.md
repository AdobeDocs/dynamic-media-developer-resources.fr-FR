---
description: Active l’optimisation de FXG.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 3%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Active l’optimisation de FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Supprime les éléments dont la visibilité est définie sur false dans FXG tout en transmettant ce FXG, ce qui réduit à son tour le temps de traitement de FXG. Bien qu’il supprime uniquement les éléments dont la visibilité est définie sur false, ce qui n’aurait aucun impact sur un autre élément dans FXG. Par exemple, s’il y a du texte sur `Path` et que la visibilité de `Path` est définie sur false, elle n’est pas supprimée de FXG même si ce modificateur est activé, car le texte doit être tracé sur ce chemin.

Par défaut : 1.
