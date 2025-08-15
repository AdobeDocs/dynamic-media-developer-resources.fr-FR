---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> valeur </span></span> </p> </td> 
   <td colname="col2"> <p> Représente le nombre maximal d'images à précharger dans chaque direction lorsque le SpinView est inactif. Une valeur de <span class="codeph"> -1</span> précharge toutes les images du jeu. Les images préchargées sont toujours affichées à la résolution d’origine du chargement initial du SpinView. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Contrôle la qualité des images préchargées. Lorsque la valeur est définie sur <span class="codeph"> 1</span> les images se chargent en haute qualité, correspondant à la taille du composant. Lorsque la valeur est définie sur <span class="codeph"> 0</span> seule la mosaïque d’aperçu basse résolution est chargée. </p> <p>Le préchargement en haute résolution améliore l’expérience de l’utilisateur final, en particulier lorsque la rotation automatique est activée. Dans le même temps, cela entraîne un temps de démarrage plus lent et une consommation réseau plus élevée. Soyez donc prudent. Lorsqu’une précharge haute résolution est utilisée, les images préchargées sont toujours à la résolution d’origine à laquelle le composant a été initialement chargé. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
