---
title: SpinView.maxloadradius
description: Représente le nombre maximal d'images à précharger dans chaque direction lorsque le SpinView est inactif.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

Représente le nombre maximal d&#39;images à précharger dans chaque direction lorsque le SpinView est inactif.

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> valeur </span></span> </p> </td> 
   <td colname="col2"> <p> Une valeur de <span class="codeph"> -1</span> précharge toutes les images du jeu. Les images préchargées sont toujours affichées à la résolution d’origine du chargement initial du SpinView. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Contrôle la qualité des images préchargées. </p> <p>Lorsque cette valeur est définie sur <span class="codeph"> 1</span> les images se chargent en haute qualité, correspondant à la taille du composant. </p> <p>Lorsque la valeur est définie sur <span class="codeph"> 0</span> seule la mosaïque d’aperçu basse résolution est chargée.</p> <p>Le préchargement en haute résolution améliore l’expérience de l’utilisateur, en particulier lorsque la rotation automatique est activée. Dans le même temps, cela ralentit le temps de démarrage et augmente la consommation du réseau. Il convient donc de l’utiliser avec précaution. Lorsque la précharge haute résolution est utilisée, les images préchargées sont toujours dans la résolution d’origine à laquelle le composant a été initialement chargé. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
