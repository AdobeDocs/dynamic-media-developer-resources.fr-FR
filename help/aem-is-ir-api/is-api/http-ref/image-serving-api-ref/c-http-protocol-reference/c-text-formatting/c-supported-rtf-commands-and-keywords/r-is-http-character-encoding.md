---
title: Encodage des caractères
description: Utilisez les commandes suivantes pour le codage des caractères.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 2%

---

# Encodage des caractères{#character-encoding}

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
   <td> <p>Caractère simple 8 bits. </p> </td> 
   <td> <p><span class="varname"> HH</span> doit être une valeur hexadécimale de 2 chiffres. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>Caractère Unicode unique. </p> </td> 
   <td> <p><span class="varname"> N</span> est un entier signé de 2 octets. Par conséquent, une valeur Unicode supérieure à 32767 doit être exprimée en nombre négatif. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Taille des caractères Unicode. </p> </td> 
   <td> <p>Nombre d’octets correspondant à un caractère Unicode donné. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>Caractères de la zone à faible résolution ANSI. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>Caractères de la zone ANSI élevée. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>Les caractères à deux octets suivent. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
