---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`xSensibilité`*[, *`ySensibilité`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[, <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Contrôle la sensibilité de la rotation horizontale et verticale effectuée avec un glissement ou un glissement de souris. </p> <p> <span class="codeph"> xSensitivity</span> définit le nombre de rotations de produit horizontales complètes effectuées si l’utilisateur fait glisser sa souris horizontalement d’un côté à l’autre de la vue. Par exemple, la valeur trois signifie que l’utilisateur voit trois rotations complètes pour un mouvement de glisser-déposer complet. </p> <p>De même, <span class="codeph"> Sensibilité</span> contrôle la sensibilité de la rotation verticale. Une valeur égale à 1 signifie qu'un glissement ou un glissement vertical complet modifie l'angle d'affichage du plan de rotation le plus haut au plus bas (ou inversement). </p> <p>Définir une valeur négative pour <span class="codeph"> Sensibilité</span> inverse la direction de la rotation verticale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
