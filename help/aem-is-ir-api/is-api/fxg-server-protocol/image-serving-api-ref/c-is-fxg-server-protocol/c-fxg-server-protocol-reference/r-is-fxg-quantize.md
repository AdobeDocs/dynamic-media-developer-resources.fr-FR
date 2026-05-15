---
title: quantifier
description: Quantification des couleurs. Indique les attributs de quantification des couleurs pour la conversion de sortie GIF.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
TQID: 'https://experienceleague.adobe.com/m5e14tLMY1JAdZTzlw7iUZzXzL9yylP66MYi5XAeYtg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# quantifier{#quantize}

Quantification des couleurs. Indique les attributs de quantification des couleurs pour la conversion de sortie GIF.

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> type de palette de </span> {adaptive|web|mac} </p> <p>Sélectionnez ' <span class="codeph"> web </span>' ou ' <span class="codeph"> mac </span>' pour choisir une palette prédéfinie, ou définissez sur ' <span class="codeph"> adaptive </span>' pour calculer une palette optimale pour l’image. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dither </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> les options de tramage {diffuse|off} </span> </p> <p>Sélectionnez « diffuse » pour la diffusion d’erreur de Floyd-Steinberg ou « désactivé » pour désactiver le tramage. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de couleurs de sortie (entier) incluses dans la palette ' <span class="codeph"> adaptive </span>'. </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> doit être compris entre 2 et 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>Liste séparée par des virgules de couleurs RGB forcées au format hex6. Permet de spécifier des couleurs forcées à inclure dans une palette « <span class="codeph"> de </span> adaptatifs ». Si le nombre de couleurs spécifié est inférieur au </span> numColors <span class="codeph">, les couleurs supplémentaires sont calculées en fonction du contenu de l’image. </p> <p>Utilisé uniquement si <span class="codeph"> fmt=gif </span> ou <span class="codeph"> fmt=gif-alpha </span>. Ignoré sinon. Les couleurs spécifiées avec <span class="codeph"> <span class="varname"> colorList </span> </span> doivent être des valeurs RGB au format hex6 (voir <span class="codeph"> des </span> de couleur) ; aucun autre spécificateur de couleur n’est autorisé. </p> </td> 
 </tr> 
</table>

## Par défaut {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Exemple {#section-b3a979dc9ae3459baa093bf17310988f}

Générez une miniature GIF à l’aide de la palette « `web` » et sans tramage :

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

Convertissez l’image en GIF bicolore avec transparence des couleurs de touches et forcez les couleurs en noir et blanc :

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
