---
description: Quantification des couleurs. Spécifie les attributs de quantification des couleurs pour la conversion de sortie GIF.
seo-description: Quantification des couleurs. Spécifie les attributs de quantification des couleurs pour la conversion de sortie GIF.
seo-title: quantifier
solution: Experience Manager
title: quantifier
uuid: 624cdc45-51f2-4b18-a658-311770974521
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# quantifier{#quantize}

Quantification des couleurs. Spécifie les attributs de quantification des couleurs pour la conversion de sortie GIF.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Type de  </span> palette {adaptive|web|mac} </p> <p>Sélectionnez " <span class="codeph"> web </span>" ou " <span class="codeph"> mac </span>" pour choisir une palette prédéfinie ou définissez " <span class="codeph"> adaptatif </span>" pour calculer une palette optimale pour l’image. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dither  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Options de  </span> tramage {diffus|off} </p> <p>Sélectionnez "diffus" pour la diffusion d'erreur Floyd-Steinberg ou "off" pour désactiver l'entrelacement. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de couleurs de sortie (entier) incluses dans la palette adaptative <span class="codeph"> </span>. </p> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> doit être compris entre 2 et 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>Liste séparée par des virgules des couleurs RVB forcées au format hex6. Permet de spécifier les couleurs forcées à inclure dans une palette " <span class="codeph"> adaptative </span>". Si le nombre de couleurs spécifié est inférieur à <span class="codeph"> numColors </span>, les couleurs supplémentaires sont calculées en fonction du contenu de l’image. </p> <p>Utilisé uniquement si <span class="codeph"> fmt=gif </span> ou <span class="codeph"> fmt=gif-alpha </span>. Ignoré autrement. Les couleurs spécifiées avec <span class="codeph"> <span class="varname"> colorList </span> </span> doivent être des valeurs RVB au format hex6 (voir <span class="codeph"> color </span>); aucun autre spécificateur de couleur n'est autorisé. </p> </td> 
 </tr> 
</table>

## Par défaut {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Exemple {#section-b3a979dc9ae3459baa093bf17310988f}

Générez une miniature GIF à l’aide de la palette &quot; `web`&quot; et sans tramage :

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

Convertir l’image en un fichier GIF bitonal avec transparence de couleur clé et forcer les couleurs en noir et blanc :

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
