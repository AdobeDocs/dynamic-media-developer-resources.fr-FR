---
title: SpinView.sensitive
description: SpinView.sensitive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
TQID: 'https://experienceleague.adobe.com/xRqLAbFehJYLGgevPmISxILSWWyedyBSDkbNZTDs808'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# SpinView.sensitive{#spinview-sensitivity}

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
