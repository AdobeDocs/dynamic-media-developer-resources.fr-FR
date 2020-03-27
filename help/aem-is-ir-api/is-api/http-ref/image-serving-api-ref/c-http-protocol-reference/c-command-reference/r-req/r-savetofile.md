---
description: Enregistrer l’image dans le fichier.
seo-description: Enregistrer l’image dans le fichier.
seo-title: saveToFile
solution: Experience Manager
title: saveToFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 32a56d77-89e2-4f78-9fab-1b528e9a024a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveToFile{#savetofile}

Enregistrer l’image dans le fichier.

`req=saveToFile&name= *``*[&timeout= *`fileval`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p> </td> 
  <td class="stentry"> <p>Chemin d’accès relatif au fichier image  du. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Intervalle d’expiration (millisecondes). </p></td> 
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
   <td> <p> <span class="codeph"> lastUpdate</span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p>Heure de création du fichier (nombre de millisecondes depuis minuit, 1er janvier 1970 UTC/GMT ). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelTotal</span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p> Nombre de pixels dans l’image enregistrée. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> état</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> effectué</span> en cas de réussite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Renvoie l’état de la réponse HTTP 200 en cas de succès et 403 en cas d’échec ou d’expiration de la requête. La réponse est de type MIME `text/plain` et ne peut pas être mise en cache.

Important L’enregistrement dans les fichiers doit être activé en spécifiant le chemin d’accès à un dossier accessible en écriture existant dans `attribute::SavePath`. `saveToFile=` échoue si `attribute::SavePath` est vide.

*`file`* est obligatoire et doit être un chemin relatif combiné à `attribute::SavePath`. Image Serving ne crée pas de dossiers. Le dossier  doit exister sur le serveur et disposer des paramètres d’autorisation appropriés pour que Image Serving crée des fichiers.

`timeout=` est facultative. Le délai d’expiration par défaut est de 60 000 msec, ou la valeur qui est configurée avec `PS::SaveTimeout`.
