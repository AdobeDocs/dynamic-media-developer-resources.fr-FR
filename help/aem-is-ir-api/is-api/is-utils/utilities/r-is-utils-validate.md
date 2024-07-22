---
description: Utilitaire de validation des images. Cet utilitaire de ligne de commande vérifie les fichiers image pour s’assurer qu’ils sont valides et que le serveur d’images peut les lire sans difficulté.
solution: Experience Manager
title: valider
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 1%

---

# valider{#validate}

Utilitaire de validation des images. Cet utilitaire de ligne de commande vérifie les fichiers image pour s’assurer qu’ils sont valides et qu’ils peuvent être lus par le serveur d’images sans difficulté.

Tous les fichiers image non PTIFF doivent être validés avant que le fichier ne soit mis à disposition du serveur d’images en tant qu’image source. Les images PTIFF doivent être validées après des opérations de copie potentiellement non fiables.

## Utilisation {#usage}

` validate *`fileType`* [ *`options`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any </span> </p> <p>Type de fichier Source ; au moins un doit être spécifié (-any autorise les mêmes types de fichiers image pris en charge par IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> options </span> </span> </p> </td> 
  <td class="stentry"> <p>Autres options de commande (voir ci-dessous). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span> </span> </p> </td> 
  <td class="stentry"> <p> Fichier image. Aucun ou plusieurs, séparés par des espaces. </p> </td> 
 </tr> 
</table>

## Renvoie {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 en cas de réussite. Si une erreur se produit, une valeur non nulle est renvoyée et les détails de l’erreur sont envoyés à `stderr`.

## Options {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>Spécifie un fichier texte distinct contenant la liste des fichiers image. Un enregistrement par fichier. Si <span class="codeph"> -fileList </span> est inclus, <span class="varname"> sourceFile </span> ne doit pas être spécifié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>Permet la vérification de l’intégralité du fichier image. Par défaut, seul l’en-tête de l’image est validé. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>Vérifie la validité du profil colorimétrique incorporé. Par défaut, le profil du corps n’est pas coché. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> Rejette les images avec 16 bits par composant d’image. Toujours spécifié par le serveur d’images lorsqu’il valide des images source distantes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> Imprime plus d’informations si l’image n’est pas valide. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent </span> </p> </td> 
  <td class="stentry"> <p>Désactive la sortie <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>. Seul un état est renvoyé. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>Termine le traitement lorsqu’un échec de validation de fichier se produit, même si des fichiers supplémentaires doivent encore être validés. Par défaut, le traitement se poursuit lorsqu’une erreur de validation se produit </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version </span> </p> </td> 
  <td class="stentry"> <p>Renvoie les informations de version de cet utilitaire. Spécifiez sans aucune autre option. </p> </td> 
 </tr> 
</table>
