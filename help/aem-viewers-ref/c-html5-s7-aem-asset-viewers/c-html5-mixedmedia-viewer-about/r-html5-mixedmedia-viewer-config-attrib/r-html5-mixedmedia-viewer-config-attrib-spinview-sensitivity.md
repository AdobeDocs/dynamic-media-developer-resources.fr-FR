---
description: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xSensitivitySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensibilité</span>[,  <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Contrôle la sensibilité de la rotation horizontale et verticale effectuée par un glissement ou un glissement de la souris. </p> <p> <span class="codeph"> </span> xSensitivitydéfinit le nombre de rotations de produits horizontales complètes qui s’effectuent si l’utilisateur fait glisser sa souris horizontalement d’un côté de la vue vers l’autre. Par exemple, trois signifie que l’utilisateur voit trois rotation complètes pour un seul mouvement de glisser. </p> <p>De même, <span class="codeph"> la sensibilité</span> contrôle la sensibilité de la rotation verticale. Une valeur de 1 signifie qu’un glissement vertical complet modifie l’angle de vue du plan de rotation le plus haut vers le plus bas (ou vice versa). </p> <p>La définition d’une valeur négative pour <span class="codeph"> la sensibilité</span> inverse la direction de la rotation verticale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
