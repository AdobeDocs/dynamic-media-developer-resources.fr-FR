---
description: Utilisez les commandes suivantes pour le codage des caractères.
seo-description: Utilisez les commandes suivantes pour le codage des caractères.
seo-title: Codage des caractères
solution: Experience Manager
title: Codage des caractères
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b19b831-b40c-4f26-83a4-732c578dbbf0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Character encoding{#character-encoding}

Utilisez les commandes suivantes pour le codage des caractères.

<table id="table_EB0C1B674BEA4A37964FB4BF559E0005"> 
 <thead> 
  <tr> 
   <th class="entry"> Commande </th> 
   <th class="entry"> Description </th> 
   <th class="entry"> Remarques </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph">\'<span class="varname"> HH</span></span> </td> 
   <td> <p>Caractère 8 bits unique. </p> </td> 
   <td> <p><span class="varname"> Il</span> doit être une valeur hexadécimale de 2 chiffres. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>Caractère Unicode unique. </p> </td> 
   <td> <p><span class="varname"> N</span> est un entier signé de 2 octets et donc une valeur Unicode supérieure à 32767 doit être exprimée en nombre négatif. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Taille de caractère Unicode. </p> </td> 
   <td> <p>Nombre d’octets correspondant au caractère Unicode donné. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>Les caractères de la zone basse ANSI suivent. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>Suivez les caractères de la zone ANSI élevée. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>Les caractères -octets suivent. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

