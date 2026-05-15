---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
TQID: 'https://experienceleague.adobe.com/eTB-wD8G7HGSDgohQn-FsCeFL1GHMBiqzNUtT3nw5n4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 127
ht-degree: 3%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Spécifie s'il faut autoriser un changement de direction de rotation en cas de visionneuse à 360° 2D. </p> <p>Lorsqu’il est défini sur <span class="codeph"> 1 </span>, le composant identifie la direction principale de glissement ou de glissement (horizontale ou verticale) au début du mouvement. Après cela, il maintient cette direction jusqu'à la fin du geste. Par exemple, si l’utilisateur ou l’utilisatrice lance une rotation horizontale, puis décide de continuer son mouvement de déplacement dans une direction verticale, le composant n’effectue pas de rotation verticale. Au lieu de cela, il ne prend en compte que le mouvement horizontal de la souris ou du balayage. </p> <p>Une valeur de <span class="codeph"> 0 </span> permet à l’utilisateur de modifier la direction de rotation à tout moment au cours de la progression du mouvement. Le paramètre n’a aucun effet si la visionneuse à 360° est 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
