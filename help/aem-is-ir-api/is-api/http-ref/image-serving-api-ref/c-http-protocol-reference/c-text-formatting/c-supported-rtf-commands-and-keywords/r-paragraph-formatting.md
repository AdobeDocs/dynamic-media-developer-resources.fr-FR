---
description: Les commandes de formatage de paragraphe suivantes sont prises en charge.
solution: Experience Manager
title: Formatage des paragraphes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# Formatage des paragraphes{#paragraph-formatting}

Les commandes de formatage de paragraphe suivantes sont prises en charge.

<table id="table_5DD044E1C0614A29A2413557DF57197D"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Commande </p> </th> 
   <th class="entry"> <p>Description </p> </th> 
   <th class="entry"> <p>Remarques </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \pard  </span> </td> 
   <td> <p>Rétablit la mise en forme des paragraphes par défaut. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql  </span> </td> 
   <td> <p>Aligne le texte à gauche. </p> </td> 
   <td> <p>Par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr  </span> </td> 
   <td> <p>Aligne le texte à droite. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc  </span> </td> 
   <td> <p>Centrer le texte horizontalement. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj  </span> </td> 
   <td> <p>Justifie le texte horizontalement. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql  </span> </td> 
   <td> <p>Aligne à gauche la dernière ligne d’un paragraphe. </p> </td> 
   <td> <p>Par défaut ; <span class="codeph"> textPs= </span> uniquement; ignoré si <span class="codeph"> \qj </span>n’est pas principal. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr  </span> </td> 
   <td> <p>Aligne à droite la dernière ligne d’un paragraphe justifié. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> uniquement; ignoré si  <span class="codeph"> \qj  </span> n'est pas principal. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc  </span> </td> 
   <td> <p>Centre la dernière ligne d’un paragraphe justifié. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> uniquement; ignoré si  <span class="codeph"> \qj  </span>n'est pas principal. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj  </span> </td> 
   <td> <p>Sustimer (étirer) la dernière ligne d'un paragraphe justifié. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> uniquement; ignoré si  <span class="codeph"> \qj  </span>n'est pas principal. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Retrait de la première ligne. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> textPs= </span> uniquement. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Retrait à gauche. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> textPs= </span> uniquement. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Retrait à droite. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> textPs= </span> uniquement. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Espace entre les lignes. </p> </td> 
   <td> <p>0 (valeur par défaut) pour l’interligne automatique ; les valeurs positives n’utilisent la valeur que si elle est supérieure à l’interligne par défaut ; valeur négative pour forcer l’espacement. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Interligne de plusieurs indicateurs. </p> </td> 
   <td> <p>Définissez sur 0 (par défaut) si <span class="codeph"> \sl </span> est en twips, sur 1 si <span class="codeph"> \sl </span> est en multiples de l’espacement par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Espace supplémentaire avant le paragraphe. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> text= </span>applique <span class="codeph"> \sb </span> au premier paragraphe de la zone de texte, <span class="codeph"> textPs= </span> ne s'applique pas. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Espace supplémentaire après le paragraphe. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> text= </span> s'applique <span class="codeph"> \sa </span> au dernier paragraphe de la zone de texte, <span class="codeph"> textPs= </span> ne s'applique pas. </p> </td> 
  </tr> 
 </tbody> 
</table>

