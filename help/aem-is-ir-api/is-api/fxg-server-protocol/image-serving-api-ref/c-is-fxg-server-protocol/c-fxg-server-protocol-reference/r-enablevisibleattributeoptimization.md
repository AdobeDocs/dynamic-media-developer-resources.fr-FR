---
description: Active l’optimisation du format FXG.
seo-description: Active l’optimisation du format FXG.
seo-title: enableVisibleAttributeOptimization
solution: Experience Manager
title: enableVisibleAttributeOptimization
topic: Scene7 Image Serving - Image Rendering API
uuid: 7f79aa12-6364-4b34-b547-88d4a778c015
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Active l’optimisation du format FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Supprime les éléments dont la visibilité est définie sur false dans FXG lors de la transmission de ce fichier FXG, ce qui réduit le temps de traitement du fichier FXG. Bien qu’il supprime uniquement les éléments dont la visibilité est définie sur false et qui n’affecteraient aucun autre élément du fichier FXG. Par exemple, si du texte est activé `Path` et que la visibilité de `Path` est définie sur false, elle n’est pas supprimée du fichier FXG même si ce modificateur est activé, car le texte doit être tracé sur ce chemin.

Valeur par défaut : 1.
