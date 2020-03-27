---
description: Utilitaire de validation d’image. Cet utilitaire de ligne de commande vérifie les fichiers image pour s’assurer qu’ils sont valides et qu’ils peuvent être lus sans difficulté par la diffusion d’images.
seo-description: Utilitaire de validation d’image. Cet utilitaire de ligne de commande vérifie les fichiers image pour s’assurer qu’ils sont valides et qu’ils peuvent être lus sans difficulté par la diffusion d’images.
seo-title: valider
solution: Experience Manager
title: valider
topic: Scene7 Image Serving - Image Rendering API
uuid: 87a129ed-950a-4b1a-9240-bf567cd8e38f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# valider{#validate}

Utilitaire de validation d’image. Cet utilitaire de ligne de commande vérifie les fichiers image pour s’assurer qu’ils sont valides et qu’ils peuvent être lus sans difficulté par la diffusion d’images.

Tous les fichiers d’image non PTIFF doivent être validés avant que le fichier ne soit rendu disponible pour Image Serving en tant qu’image source. Les images PTIFF doivent être validées après des opérations de copie potentiellement non fiables.

## Utilisation {#usage}

` validate *``* [ *``*] [ *`fileTypeoptionssourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg| -ptif| -any </span> </p> <p>type de fichier source ; au moins un doit être spécifié (-any autorise les mêmes types de fichiers image pris en charge par IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> options </span></span> </p> </td> 
  <td class="stentry"> <p>Autres options de commande (voir ci-dessous). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fichier source </span></span> </p> </td> 
  <td class="stentry"> <p> Fichier image. Aucun ou plus, séparés par des espaces. </p> </td> 
 </tr> 
</table>

## Returns {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 en cas de succès. Si une erreur se produit, une valeur non nulle est renvoyée et les détails de l’erreur sont envoyés à `stderr`.

## Options {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span></span> </p> </td> 
  <td class="stentry"> <p>Spécifie un fichier texte distinct contenant le  des fichiers image. Un enregistrement par fichier. Si <span class="codeph"> -fileList </span> est inclus, <span class="varname"> le fichier source </span> ne doit pas être spécifié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>Permet la vérification de l’intégralité du fichier image. Par défaut, seul l’en-tête de l’image est validé. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>Vérifie la validité du de couleurs incorporé. Par défaut, le corps  du n’est pas coché. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fail16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> Rejette les images avec 16 bits par composant d’image. Toujours spécifié par le serveur d’images lorsqu’il valide les images source distantes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> Imprime plus d’informations si l’image n’est pas valide. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silence </span> </p> </td> 
  <td class="stentry"> <p>Désactive la sortie <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span> . Seul un état est renvoyé. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>Termine le traitement en cas d’échec de validation d’un fichier, même si des fichiers supplémentaires doivent encore être validés. Par défaut, le traitement se poursuit lorsqu’une erreur de validation se produit </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version </span> </p> </td> 
  <td class="stentry"> <p>Renvoie les informations de version pour cet utilitaire. Spécifiez sans autres options. </p> </td> 
 </tr> 
</table>

