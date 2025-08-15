---
description: Utilitaire de validation d’images. Cet utilitaire de ligne de commande vérifie les fichiers image pour s’assurer qu’ils sont valides et que Image Serving peut les lire sans difficulté.
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

Utilitaire de validation d’images. Cet utilitaire de ligne de commande vérifie les fichiers image pour s’assurer qu’ils sont valides et peuvent être lus par Image Serving sans difficulté.

Tous les fichiers image non PTIFF doivent passer la validation avant d’être mis à la disposition de l’image servant d’image source. Les images PTIFF doivent être validées après des opérations de copie potentiellement peu fiables.

## Utilisation {#usage}

` validate *`fileType`* [ *`options`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Type de </span> fichier </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -quelconque </span> </p> <p>Type de fichier source ; au moins un doit être spécifié (-any autorise les mêmes types de fichiers image pris en charge par IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Options </span> </span> </p> </td> 
  <td class="stentry"> <p>Autres options de commande (voir ci-dessous). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Fichier </span> source </span> </p> </td> 
  <td class="stentry"> <p> Fichier image. Aucun ou plus, séparés par des espaces. </p> </td> 
 </tr> 
</table>

## Retourne {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 en cas de réussite. Si une erreur survient, une valeur différente de zéro est renvoyée et les détails de l’erreur sont envoyés à `stderr`.

## Options {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList, <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>Spécifie un fichier texte distinct contenant la liste des fichiers image. Un enregistrement par fichier. Si <span class="codeph"> -fileList </span> est inclus, <span class="varname"> sourceFile </span> ne doit pas être spécifié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>Permet de vérifier l’intégralité du fichier image. Par défaut, seul l’en-tête de l’image est validé. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>Vérifie la validité du profil de couleurs incorporé. Par défaut, le profil corporel n’est pas vérifié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> Rejette les images avec 16 bits par composant d’image. Toujours indiqué par le serveur d’images lors de la validation des images sources distantes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbeux </span> </p> </td> 
  <td class="stentry"> <p> Imprime plus d’informations si l’image n’est pas valide. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silencieux </span> </p> </td> 
  <td class="stentry"> <p>Désactive la <span class="codeph"> sortie stdout/ </span> stderr<span class="codeph"></span>. Seul un statut est renvoyé. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>Met fin au traitement lorsqu’un échec de validation de fichier se produit, même si des fichiers supplémentaires doivent encore être validés. Par défaut, le traitement se poursuit lorsqu’une erreur de validation se produit </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -Version </span> </p> </td> 
  <td class="stentry"> <p>Renvoie les informations de version pour cet utilitaire. Spécifiez sans autre option. </p> </td> 
 </tr> 
</table>
