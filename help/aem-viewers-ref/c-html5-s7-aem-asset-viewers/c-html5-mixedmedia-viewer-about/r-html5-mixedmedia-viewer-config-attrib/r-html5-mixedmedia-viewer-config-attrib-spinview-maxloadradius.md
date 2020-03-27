---
description: Représente le nombre maximal d’images à précharger dans chaque direction lorsque la vue à 360° est inactive.
seo-description: Représente le nombre maximal d’images à précharger dans chaque direction lorsque la vue à 360° est inactive.
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: e1b9fa84-837c-465e-8d37-0b6867404cae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.maxloadradius{#spinview-maxloadradius}

Représente le nombre maximal d’images à précharger dans chaque direction lorsque la vue à 360° est inactive.

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> La valeur <span class="codeph"> -1</span> précharge toutes les images de la visionneuse. Les images préchargées sont toujours affichées à la résolution d’origine du chargement initial de la vue à 360°. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Contrôle la qualité des images préchargées. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> 1</span> , les images se chargent en haute qualité, en fonction de la taille du composant. </p> <p>Lorsque cette valeur est définie sur <span class="codeph"> 0</span> , seule la mosaïque de basse résolution est chargée. </p> <p>Le préchargement en haute résolution améliore l’expérience de l’utilisateur final, en particulier lorsque la rotation automatique est activée. Dans le même temps, il se traduit par un temps de plus lent et une consommation réseau plus élevée. Il doit donc être utilisé avec soin. Lorsque le préchargement haute résolution est utilisé, les images préchargées sont toujours dans la résolution d’origine à laquelle le composant a été initialement chargé. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
