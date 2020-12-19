---
description: 'null'
seo-description: 'null'
seo-title: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
topic: Dynamic media
uuid: 82cf1f26-3af0-494f-b918-fdc318959c75
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 5%

---


# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xSensitivityySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[,  <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Contrôle la sensibilité de la rotation horizontale et verticale effectuée avec un glissement ou un glissement de la souris. </p> <p> <span class="codeph"> </span> xSensitivitydéfinit le nombre de rotations de produits horizontales complètes si l'utilisateur fait glisser sa souris horizontalement d'un côté à l'autre de la vue. Par exemple, trois signifie que l’utilisateur voit trois spins complets pour un mouvement de glissement complet. </p> <p>De même, <span class="codeph"> ySensitivity</span> contrôle la sensibilité de la rotation verticale. Une valeur de 1 signifie qu’un glissement ou un glissement vertical complet modifie l’angle de vue du plan de rotation le plus élevé au plan de rotation le plus bas (ou vice versa). </p> <p>La définition d’une valeur négative pour <span class="codeph"> ySensitivity</span> inverse la direction de la rotation verticale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
