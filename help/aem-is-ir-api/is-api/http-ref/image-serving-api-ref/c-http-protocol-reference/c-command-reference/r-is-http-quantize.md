---
description: Quantification des couleurs. Spécifie les attributs de quantification des couleurs pour la conversion de sortie GIF.
seo-description: Quantification des couleurs. Spécifie les attributs de quantification des couleurs pour la conversion de sortie GIF.
seo-title: quantifier
solution: Experience Manager
title: quantifier
topic: Scene7 Image Serving - Image Rendering API
uuid: 4e9c4807-59bc-4eb9-bcab-0bf0cfdf56d4
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# quantifier{#quantize}

Quantification des couleurs. Spécifie les attributs de quantification des couleurs pour la conversion de sortie GIF.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>Indique le type de palette. </p> <p>Définissez cette option sur <span class="codeph"> adaptatif </span> pour calculer une palette optimale pour l’image. </p> <p>Définissez cette option sur le <span class="codeph"> Web </span> ou <span class="codeph"> Mac </span> pour choisir une palette prédéfinie. </p> <p> <p>Remarque :  Le <span class="codeph"> type de </span> palette mac est uniquement pris en charge pour les formats GIF et PNG8, mais pas pour les formats GIF-Alpha et PNG8-Alpha. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dither </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>Spécifie les options de tramage. </p> <p>Définir pour <span class="codeph"> diffuser </span> la diffusion de l'erreur Floyd-Steinberg </p> <p>Définissez cette option sur <span class="codeph"> Désactivé </span> pour désactiver l’interpolation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span></span> </p> </td> 
   <td colname="col2"> <p>Nombre de couleurs de sortie (2-256) </p> <p>Indique le nombre de couleurs incluses dans la <span class="codeph"> palette </span> adaptative. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span></span> </p> </td> 
   <td colname="col2"> <p>de couleurs RVB forcées au format hexadécimal, séparé par des virgules </p> <p>Permet de spécifier les couleurs à inclure dans une <span class="codeph"> palette </span> adaptative. Si le nombre de couleurs spécifié est inférieur à <span class="codeph"> numColors <span class="varname"> </span> </span>, des couleurs supplémentaires sont calculées en fonction du contenu de l’image. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-8ab5035055b24b858270d260912a7f3d}

Attribut de requête. S’applique indépendamment du paramètre de calque actif. Utilisé uniquement si `fmt=gif`, `fmt=gif-alpha`, `fmt=png8`ou `fmt=png8-alpha`. Ignoré autrement.

Les couleurs spécifiées avec ` *`colorList`*` doivent être composées de valeurs RVB au format hex6 (voir ` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`) sans préfixe &quot; `0x`&quot;. Aucun autre spécificateur de couleur n’est autorisé. *`numColors`* doit être compris entre 2 et 256.

## Par défaut {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Exemple {#section-e34aca7587d548a7ae9d4266b80c9451}

Générez une miniature GIF à l’aide de la `web` palette et sans tramage :

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Convertir l’image en un fichier GIF bitonal avec transparence de couleur clé et forcer les couleurs en noir et blanc :

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Voir aussi {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
