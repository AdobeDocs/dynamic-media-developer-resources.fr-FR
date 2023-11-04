---
title: SpinView.iconeffect
description: SpinView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 473207d2-7e26-4ea3-940e-5a21f29a2b91
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 4%

---

# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_DF2137DF9C7441B381D2B03CEE4B880A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Active la variable <span class="codeph"> iconEffet</span> s’affiche en haut de l’image lorsque celle-ci est à l’état réinitialisé et indique qu’une action peut être effectuée pour interagir avec l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> nombre</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le nombre maximal de fois que la variable <span class="codeph"> iconEffet</span> apparaît et réapparaît. Une valeur de <span class="codeph"> -1</span> indique que l’icône réapparaît toujours indéfiniment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p>Indique la durée de l’animation d’affichage ou de masquage, en secondes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Définit le nombre de secondes pendant lesquelles la variable <span class="codeph"> iconEffet</span> reste entièrement visible avant son masquage automatique. C’est-à-dire le temps qui suit la fin de l’animation en fondu, mais avant que l’animation en fondu ne commence. Un paramètre de <span class="codeph"> 0</span> désactive le comportement de masquage automatique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
