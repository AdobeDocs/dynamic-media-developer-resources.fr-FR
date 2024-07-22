---
title: quantifier
description: Quantification des couleurs. Spécifie les attributs de quantification des couleurs pour la conversion de sortie de GIF.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# quantifier{#quantize}

Quantification des couleurs. Spécifie les attributs de quantification des couleurs pour la conversion de sortie de GIF.

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>Indique le type de palette. </p> <p>Définissez cette variable sur <span class="codeph"> adaptatif </span> pour calculer une palette optimale pour l’image. </p> <p>Définissez cette variable sur <span class="codeph"> web </span> ou <span class="codeph"> mac </span> pour choisir une palette prédéfinie. </p> <p> <p>Remarque : Le type de palette <span class="codeph"> mac </span> n’est pris en charge que pour les formats GIF et PNG8, mais pas pour les formats d’Alpha GIF et d’Alpha PNG8.</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dither </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffusion|off} </span> </p> <p>Spécifie les options de tramage. </p> <p>Définissez cette variable sur <span class="codeph"> diffus </span> pour la diffusion de l’erreur Floyd-Steinberg. </p> <p>Définissez cette variable sur <span class="codeph"> sur </span> pour désactiver le tramage.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>Nombre de couleurs de sortie (2-256) </p> <p>Indique le nombre de couleurs incluses dans la palette <span class="codeph"> adaptative </span>.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>Liste séparée par des virgules de couleurs de RGB forcées au format hexadécimal6 </p> <p>Permet de spécifier les couleurs à inclure dans une palette <span class="codeph"> adaptative </span>. Si le nombre de couleurs spécifié est inférieur à <span class="codeph"> <span class="varname"> numColors </span> </span>, les couleurs supplémentaires sont calculées en fonction du contenu de l’image.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-8ab5035055b24b858270d260912a7f3d}

Attribut de requête. Elle s’applique quel que soit le paramètre de calque actuel. Utilisé uniquement si `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` ou `fmt=png8-alpha`. Ignoré autrement.

Les couleurs spécifiées avec *`colorList`* doivent être composées de valeurs de RGB au format hex6 (voir [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) sans préfixe `0x`). Aucun autre spécificateur de couleur n’est autorisé. Le modificateur *`numColors`* doit être de 2 à 256.

## Par défaut {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Exemple {#section-e34aca7587d548a7ae9d4266b80c9451}

Générez une miniature de GIF à l’aide de la palette `web` sans tramage :

`http:// *`*Serveur*`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Convertissez l’image en GIF bimensuel avec transparence couleur-clé. Et forcer les couleurs au noir et blanc :

`http:// *`*Serveur*`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Voir aussi {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
