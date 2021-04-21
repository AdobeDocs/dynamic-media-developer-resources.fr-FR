---
description: Utilisez les commandes suivantes pour le codage des caractères.
solution: Experience Manager
title: Codage des caractères
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---


# Codage des caractères {#character-encoding}

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
   <td> <p>Caractère unique 8 bits. </p> </td> 
   <td> <p><span class="varname"> </span> HH doit être une valeur hexadécimale de 2 chiffres. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>Caractère Unicode unique. </p> </td> 
   <td> <p><span class="varname"> </span> Nis est un entier signé de 2 octets et donc une valeur Unicode supérieure à 32767 doit être exprimée en nombre négatif. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>Taille de caractère Unicode. </p> </td> 
   <td> <p>Nombre d'octets correspondant au caractère Unicode donné. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>Suivez les caractères de la zone à faible valeur ANSI. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich  </span> </td> 
   <td> <p>Suivez les caractères de la zone ANSI élevée. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>Les caractères sur doublon-octet suivent. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

