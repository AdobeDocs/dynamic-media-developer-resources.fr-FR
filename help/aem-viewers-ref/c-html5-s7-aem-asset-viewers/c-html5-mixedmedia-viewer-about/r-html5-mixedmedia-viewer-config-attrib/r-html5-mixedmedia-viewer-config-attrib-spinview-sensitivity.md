---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`xSensibilité`*[, *`ySensibilité`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensibilité</span>[, <span class="varname"> ySensibilité</span>]</span> </p> </td> 
   <td colname="col2"> <p> Contrôle la sensibilité de la rotation horizontale et verticale effectuée par un glissement ou un glissement de la souris. </p> <p> <span class="codeph"> xSensibilité</span> définit le nombre de rotations de produits horizontales complètes qui sont effectuées si l’utilisateur fait glisser sa souris horizontalement d’un côté de la vue vers l’autre. Par exemple, trois signifie que l’utilisateur voit trois rotation complètes pour un seul mouvement de glisser. </p> <p>De même, <span class="codeph"> ySensibilité</span> contrôle la sensibilité de la rotation verticale. Une valeur de 1 signifie qu’un glissement vertical complet modifie l’angle de vue du plan de rotation le plus haut vers le plan le plus bas (ou à l’inverse). </p> <p>Définition d’une valeur négative pour <span class="codeph"> ySensibilité</span> inverse la direction de la rotation verticale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
