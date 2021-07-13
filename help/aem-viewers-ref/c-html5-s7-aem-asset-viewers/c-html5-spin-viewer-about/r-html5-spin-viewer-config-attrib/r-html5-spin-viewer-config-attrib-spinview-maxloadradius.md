---
description: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses à 360°
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Représente le nombre maximal d’images à précharger dans chaque direction lorsque la vue à 360° est inactive. Une valeur <span class="codeph"> -1</span> précharge toutes les images de l’ensemble. Les images préchargées sont toujours affichées à la résolution d’origine à laquelle la vue à 360° a été initialement chargée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Contrôle la qualité des images préchargées. Lorsqu’elle est définie sur <span class="codeph"> 1</span>, les images se chargent en haute qualité, ce qui correspond à la taille du composant. Lorsqu’elle est définie sur <span class="codeph"> 0</span>, seule la mosaïque d’aperçu basse résolution est chargée. </p> <p>Le préchargement en haute résolution améliore l’expérience de l’utilisateur final, en particulier lorsque la rotation automatique est activée. Dans le même temps, cela ralentit le démarrage et augmente la consommation du réseau. Par conséquent, utilisez avec précaution. Lorsqu’un préchargement haute résolution est utilisé, les images préchargées sont toujours à la résolution d’origine à laquelle le composant a été initialement chargé. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
