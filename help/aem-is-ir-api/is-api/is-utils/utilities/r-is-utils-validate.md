---
description: Utilitaire de validation d’image. Cet utilitaire de ligne de commande vérifie les fichiers image pour s’assurer qu’ils sont valides et qu’ils peuvent être lus sans difficulté par la diffusion d’images.
solution: Experience Manager
title: valider
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# valider{#validate}

Utilitaire de validation d’image. Cet utilitaire de ligne de commande vérifie les fichiers image pour s’assurer qu’ils sont valides et qu’ils peuvent être lus sans difficulté par la diffusion d’images.

Tous les fichiers d’image non PTIFF doivent être validés avant que le fichier ne soit rendu disponible pour Image Serving en tant qu’image source. Les images PTIFF doivent être validées après des opérations de copie potentiellement non fiables.

## Utilisation {#usage}

` validate *``* [ *``*] [ *`fileTypeoptionssourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any  </span> </p> <p>type de fichier source ; au moins un doit être spécifié (-any autorise les mêmes types de fichiers image pris en charge par IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> options  </span> </span> </p> </td> 
  <td class="stentry"> <p>Autres options de commande (voir ci-dessous). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile  </span> </span> </p> </td> 
  <td class="stentry"> <p> Fichier image. Aucun ou plusieurs, séparés par des espaces. </p> </td> 
 </tr> 
</table>

## Renvoie {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 en cas de réussite. Si une erreur se produit, une valeur non nulle est renvoyée et les détails de l&#39;erreur sont envoyés à `stderr`.

## Options {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList  <span class="varname"> listFile  </span> </span> </p> </td> 
  <td class="stentry"> <p>Indique un fichier texte distinct contenant la liste des fichiers image. Un enregistrement par fichier. Si <span class="codeph"> -fileList </span> est inclus, <span class="varname"> sourceFile </span> ne doit pas être spécifié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels  </span> </p> </td> 
  <td class="stentry"> <p>Permet la vérification de l’intégralité du fichier image. Par défaut, seul l’en-tête d’image est validé. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile  </span> </p> </td> 
  <td class="stentry"> <p>Vérifie la validité du profil de couleurs incorporé. Par défaut, le corps du profil n’est pas vérifié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -rejette16BitPerComponent  </span> </p> </td> 
  <td class="stentry"> <p> Rejette les images avec un composant d’image de 16 bits. Toujours spécifié par le serveur d’images lorsqu’il valide les images source distantes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose  </span> </p> </td> 
  <td class="stentry"> <p> Imprime plus d’informations si l’image n’est pas valide. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silence  </span> </p> </td> 
  <td class="stentry"> <p>Désactive la sortie <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>. Seul un état est renvoyé. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError  </span> </p> </td> 
  <td class="stentry"> <p>Termine le traitement en cas d’échec de validation d’un fichier, même si d’autres fichiers doivent encore être validés. Par défaut, le traitement se poursuit lorsqu’une erreur de validation se produit </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version </span> </p> </td> 
  <td class="stentry"> <p>Renvoie les informations de version pour cet utilitaire. N’indiquez aucune autre option. </p> </td> 
 </tr> 
</table>

