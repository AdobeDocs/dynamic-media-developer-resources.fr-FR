---
description: Swatches.align
solution: Experience Manager
title: Swatches.align
feature: Dynamic Media Classic, Visionneuses, SDK/API, Combiner des visionneuses de supports
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---


# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Indique l’alignement interne (ancrage) du conteneur des échantillons dans la zone du composant. Dans les échantillons, le conteneur de miniature interne est dimensionné de sorte que seul un nombre entier de nuances s’affiche. En conséquence, il y a un certain remplissage entre le conteneur interne et les limites de composants externes. Cette commande indique comment le conteneur des échantillons internes est positionné à l’intérieur du composant.

<table id="table_58D88FF5F83A4ABA928695B5AFF97354"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> left|center|right</span> </p> </td> 
   <td> <p> Définit l’alignement des nuances horizontales. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><span class="codeph"> top|center|bottom</span> </p> </td> 
   <td> <p> Définit l’alignement des nuances verticales. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`center,center`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`align=left,top`
