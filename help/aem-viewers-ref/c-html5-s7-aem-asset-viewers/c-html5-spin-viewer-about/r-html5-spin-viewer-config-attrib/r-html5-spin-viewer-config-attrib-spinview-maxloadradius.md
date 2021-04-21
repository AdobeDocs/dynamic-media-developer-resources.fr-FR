---
description: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Représente le nombre maximal d’images à précharger dans chaque direction lorsque la vue à 360° est inactive. La valeur <span class="codeph"> -1</span> précharge toutes les images de l’ensemble. Les images préchargées sont toujours affichées à la résolution initiale du chargement initial de la vue à 360°. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Contrôle la qualité des images préchargées. Lorsqu’elle est définie sur <span class="codeph"> 1</span>, les images sont chargées en haute qualité, ce qui correspond à la taille du composant. Lorsqu’elle est définie sur <span class="codeph"> 0</span>, seule la mosaïque de prévisualisation basse résolution est chargée. </p> <p>Le préchargement en haute résolution améliore l’expérience de l’utilisateur final, en particulier lorsque la rotation automatique est activée. Dans le même temps, elle ralentit le début et augmente la consommation du réseau. Utilisez-la avec précaution. Lorsqu’un préchargement haute résolution est utilisé, les images préchargées sont toujours à la résolution d’origine à laquelle le composant a été initialement chargé. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
