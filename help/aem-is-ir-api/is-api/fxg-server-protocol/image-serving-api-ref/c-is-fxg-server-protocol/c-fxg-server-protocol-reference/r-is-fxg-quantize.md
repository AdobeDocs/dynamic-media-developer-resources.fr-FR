---
description: Quantification des couleurs. Spécifie les attributs de quantification des couleurs pour la conversion de sortie GIF.
seo-description: Quantification des couleurs. Spécifie les attributs de quantification des couleurs pour la conversion de sortie GIF.
seo-title: quantifier
solution: Experience Manager
title: quantifier
topic: Scene7 Image Serving - Image Rendering API
uuid: 624cdc45-51f2-4b18-a658-311770974521
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# quantifier{#quantize}

Quantification des couleurs. Spécifie les attributs de quantification des couleurs pour la conversion de sortie GIF.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Type de palette {adaptatif|web|mac} </span> </p> <p>Sélectionnez " <span class="codeph"> web </span>" ou " <span class="codeph"> mac </span>" pour choisir une palette prédéfinie ou "adaptatif <span class="codeph"> </span>" pour calculer une palette optimale pour l’image. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dither </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Options de </span> tramage {diffus|off} </p> <p>Sélectionnez "diffus" pour la diffusion d’erreur Floyd-Steinberg ou "off" pour désactiver l’interpolation. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span></span> </p> </td> 
  <td class="stentry"> <p>Nombre de couleurs de sortie (entier) incluses dans la palette <span class="codeph"> adaptative </span>. </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> doit être compris entre 2 et 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span></span> </p> </td> 
  <td class="stentry"> <p>séparé par des virgules de couleurs RVB forcées au format hexadécimal6. Permet de spécifier les couleurs forcées à inclure dans une palette " <span class="codeph"> adaptative </span>". Si le nombre de couleurs spécifié est inférieur à <span class="codeph"> numColors </span>, des couleurs supplémentaires sont calculées en fonction du contenu de l’image. </p> <p>Utilisée uniquement si <span class="codeph"> fmt=gif </span> ou <span class="codeph"> fmt=gif-alpha </span>. Ignoré autrement. Les couleurs spécifiées avec la <span class="codeph"> liste des <span class="varname"> couleurs </span> doivent être des valeurs RVB au format hex6 (voir </span> couleur <span class="codeph"> </span>) ; aucun autre spécificateur de couleur n’est autorisé. </p> </td> 
 </tr> 
</table>

## Par défaut {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Exemple {#section-b3a979dc9ae3459baa093bf17310988f}

Générez une miniature GIF à l’aide de la palette `web`&quot; et sans tramage :

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

Convertir l’image en un fichier GIF bitonal avec transparence de couleur clé et forcer les couleurs en noir et blanc :

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
