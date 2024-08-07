---
title: quantifier
description: Quantification des couleurs. Spécifie les attributs de quantification des couleurs pour la conversion de sortie de GIF.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# quantifier{#quantize}

Quantification des couleurs. Spécifie les attributs de quantification des couleurs pour la conversion de sortie de GIF.

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> type de palette </p> <p>Sélectionnez " <span class="codeph"> web </span>" ou " <span class="codeph"> mac </span>" pour choisir une palette prédéfinie ou définissez cette valeur sur " <span class="codeph"> adaptive </span>" pour calculer une palette optimale pour l’image. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dither </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffus|off} </span> options d’entrecroisement </p> <p>Sélectionnez "diffus" pour la diffusion de l’erreur Floyd-Steinberg ou "off" pour désactiver l’hésitation. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de couleurs de sortie (nombre entier) incluses dans la palette <span class="codeph"> adaptative </span>. </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> doit être compris entre 2 et 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>Liste séparée par des virgules des couleurs de RGB forcées au format hex6. Permet de spécifier les couleurs forcées à inclure dans une palette <span class="codeph"> adaptative </span>. Si le nombre de couleurs spécifié est inférieur à <span class="codeph"> numColors </span>, les couleurs supplémentaires sont calculées en fonction du contenu de l’image. </p> <p>Utilisé uniquement si <span class="codeph"> fmt=gif </span> ou <span class="codeph"> fmt=gif-alpha </span>. Ignoré autrement. Les couleurs spécifiées avec <span class="codeph"> <span class="varname"> colorList </span> </span> doivent être des valeurs RGB au format hex6 (voir <span class="codeph"> color </span>) ; aucun autre spécification de couleur n’est autorisé. </p> </td> 
 </tr> 
</table>

## Par défaut {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Exemple {#section-b3a979dc9ae3459baa093bf17310988f}

Générez une miniature de GIF à l’aide de la palette &quot; `web`&quot; et sans tramage :

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

Convertissez l’image en GIF bonal avec transparence couleur clé et forcer les couleurs en noir et blanc :

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
