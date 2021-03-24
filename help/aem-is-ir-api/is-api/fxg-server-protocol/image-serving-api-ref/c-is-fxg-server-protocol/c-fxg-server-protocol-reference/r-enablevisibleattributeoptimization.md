---
description: Active l’optimisation du fichier FXG.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Active l’optimisation du fichier FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Supprime les éléments dont la visibilité est définie sur false dans FXG lors de la transmission de ce fichier FXG, ce qui réduit à son tour le temps de traitement du fichier FXG. Bien qu’il supprime uniquement les éléments dont la visibilité est définie sur false, ce qui n’affecterait aucun autre élément dans FXG. Par exemple, s’il y a du texte sur `Path` et que la visibilité de `Path` est définie sur false, elle n’est pas supprimée du fichier FXG même si ce modificateur est activé, car le texte doit être tracé sur ce chemin.

Valeur par défaut : 1.
