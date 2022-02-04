---
title: SpinView.maxloadradius
description: Représente le nombre maximal d’images à précharger dans chaque direction lorsque la vue à 360° est inactive.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

Représente le nombre maximal d’images à précharger dans chaque direction lorsque la vue à 360° est inactive.

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Une valeur de <span class="codeph"> -1</span> précharge toutes les images de la visionneuse. Les images préchargées sont toujours affichées à la résolution d’origine à laquelle la vue à 360° a été initialement chargée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Contrôle la qualité des images préchargées. </p> <p>Lorsque la variable est définie sur <span class="codeph"> 1</span> les images se chargent en haute qualité, correspondant à la taille du composant. </p> <p>Lorsque la variable est définie sur <span class="codeph"> 0</span> seule la mosaïque d’aperçu basse résolution est chargée.</p> <p>Le préchargement en haute résolution améliore l’expérience d’un utilisateur, en particulier lorsque la rotation automatique est activée. En même temps, elle ralentit le démarrage et augmente la consommation du réseau. Elle doit donc être utilisée avec précaution. Lorsque le préchargement haute résolution est utilisé, les images préchargées sont toujours à la résolution d’origine à laquelle le composant a été initialement chargé. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
