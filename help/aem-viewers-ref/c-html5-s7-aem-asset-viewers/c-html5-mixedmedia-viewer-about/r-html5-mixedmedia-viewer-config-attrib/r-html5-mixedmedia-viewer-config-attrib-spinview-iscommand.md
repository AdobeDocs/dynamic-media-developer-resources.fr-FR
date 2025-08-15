---
title: SpinView.iscommand
description: SpinView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: d616c8cf-6717-48f9-9926-1b37afe0e444
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---

# SpinView.iscommand{#spinview-iscommand}

` [SpinView.|<containerId>_spinView.]iscommand= *`Commande isCommand`*`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Commande isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Chaîne de commande de diffusion d’images appliquée à la rotation de l’image. Si elles sont spécifiées dans l’URL, toutes les occurrences de &amp; et = doivent être codées en HTTP en tant que <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>, respectivement.<span class="codeph"> </span><span class="codeph"> </span> </p> <p> <p>Remarque : les commandes de manipulation de dimensionnement d’image ne sont pas prises en charge. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Aucune

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

Lorsque cela est spécifié dans l’URL de la visionneuse :

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Lorsque cela est spécifié dans les données de configuration :

`iscommand=op_sharpen=1&op_colorize=0xff0000`
