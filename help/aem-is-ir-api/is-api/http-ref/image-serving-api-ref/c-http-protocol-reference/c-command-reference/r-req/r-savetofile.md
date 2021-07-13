---
description: Enregistrez l’image dans le fichier .
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---

# saveToFile{#savetofile}

Enregistrez l’image dans le fichier .

`req=saveToFile&name= *``*[&timeout= *`fileval`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p> </td> 
  <td class="stentry"> <p>Chemin d’accès relatif au fichier image cible. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Intervalle de dépassement de délai (millisecondes). </p></td> 
 </tr> 
</table>

Enregistre l’image de réponse dans un fichier sur le serveur au lieu de la renvoyer au client.

Une fois la requête d’enregistrement terminée, elle renvoie plusieurs propriétés au format Java, notamment :

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Propriété</b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p>Heure de création du fichier (nombre de millisecondes depuis minuit, 1er janvier 1970 UTC/GMT ). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p> Nombre de pixels dans l’image enregistrée. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> état</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> </span> effectuez un suivi en cas de réussite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Renvoie l’état de réponse HTTP 200 en cas de réussite et 403 si la requête échoue ou expire. La réponse est de type MIME `text/plain` et ne peut pas être mise en cache.

Important : L’enregistrement dans les fichiers doit être activé en spécifiant le chemin d’accès à un dossier modifiable existant dans `attribute::SavePath`. `saveToFile=` échoue si  `attribute::SavePath` est vide.

*`file`* est obligatoire et doit être un chemin relatif combiné avec  `attribute::SavePath`. La diffusion d’images ne crée pas de dossiers. Le dossier cible doit exister sur le serveur et disposer des paramètres d’autorisation appropriés pour que le serveur d’images puisse créer des fichiers.

`timeout=` est facultatif. Le délai d’expiration par défaut est de 60 000 ms, ou n’importe quelle valeur est configurée avec `PS::SaveTimeout`.
