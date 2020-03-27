---
description: 'null'
seo-description: 'null'
seo-title: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
topic: Dynamic media
uuid: b46a3d78-e381-4351-a4f4-a228386df527
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Indique s’il faut autoriser un changement de direction de rotation dans le cas d’une visionneuse à 360° 2D. </p> <p>Lorsqu’il est défini sur <span class="codeph"> 1 </span>, le composant identifie la direction principale du glissement ou du glissement (horizontale par rapport à verticale) à l’ du mouvement. Après cela, il maintient cette direction jusqu'à ce que le geste se termine. Par exemple, si l’utilisateur  une rotation horizontale puis décide de poursuivre son mouvement de glissement dans une direction verticale, le composant n’effectue pas de rotation verticale ; il ne tient compte que du mouvement horizontal de la souris ou du glissement. </p> <p>La valeur <span class="codeph"> 0 </span> permet à l’utilisateur de modifier la direction de rotation à tout moment pendant la progression du mouvement. Ce paramètre n’a aucune incidence si la visionneuse à 360° est 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
