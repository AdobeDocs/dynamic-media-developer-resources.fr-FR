---
description: Utilitaire de validation des images. Cet utilitaire de ligne de commande vérifie les fichiers image pour s’assurer qu’ils sont valides et que le service d’images peut les lire sans difficulté.
solution: Experience Manager
title: valider
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
TQID: 'https://experienceleague.adobe.com/gWtVDo3ounZMncdhwLMJsoRaPyZP3E1Fi98L8fX6XFA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 281
ht-degree: 1%

---

# valider{#validate}

Utilitaire de validation des images. Cet utilitaire de ligne de commande vérifie les fichiers image pour s’assurer qu’ils sont valides et qu’ils peuvent être lus sans difficulté par le service d’images.

Tous les fichiers image non PTIFF doivent passer la validation avant que le fichier ne soit disponible pour l’image servant d’image source. Les images PTIFF doivent être validées après des opérations de copie potentiellement non fiables.

## Utilisation {#usage}

` validate *`fileType`* [ *`options`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any </span> </p> <p>Type de fichier Source ; au moins un type doit être spécifié (-any autorise les mêmes types de fichiers image pris en charge par IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> options </span> </span> </p> </td> 
  <td class="stentry"> <p>Autres options de commande (voir ci-dessous). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span> </span> </p> </td> 
  <td class="stentry"> <p> Fichier image. Aucun ou plus, séparé par des espaces. </p> </td> 
 </tr> 
</table>

## Renvoie {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 en cas de réussite. Si une erreur se produit, une valeur non nulle est renvoyée et les détails de l’erreur sont envoyés à `stderr`.

## Options {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>Spécifie un fichier texte séparé contenant la liste des fichiers image. Un enregistrement par fichier. Si <span class="codeph"> -fileList </span> est inclus, <span class="varname"> sourceFile </span> ne doit pas être spécifié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>Permet de vérifier l’intégralité du fichier image. Par défaut, seul l’en-tête de l’image est validé. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>Vérifie la validité du profil de couleurs incorporé. Par défaut, le profil du corps n’est pas coché. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -rejet16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> Rejette les images avec 16 bits par composant d’image. Toujours spécifié par le serveur d’images lors de la validation des images sources distantes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> Imprime des informations supplémentaires si l’image n’est pas valide. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent </span> </p> </td> 
  <td class="stentry"> <p>Désactive <span class="codeph"> sortie stdout </span>/ <span class="codeph"> stderr </span>. Seul un statut est renvoyé. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>Termine le traitement lorsqu’un échec de validation de fichier se produit, même si d’autres fichiers doivent encore être validés. Par défaut, le traitement se poursuit lorsqu’une erreur de validation se produit </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version </span> </p> </td> 
  <td class="stentry"> <p>Retourne les informations de version pour cet utilitaire. Spécifiez sans autre option. </p> </td> 
 </tr> 
</table>
