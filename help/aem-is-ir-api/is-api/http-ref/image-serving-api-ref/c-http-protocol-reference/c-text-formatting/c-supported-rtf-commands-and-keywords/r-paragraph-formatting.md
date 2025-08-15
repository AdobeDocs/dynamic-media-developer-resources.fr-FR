---
description: Les commandes de formatage des paragraphes suivants sont prises en charge.
solution: Experience Manager
title: Mise en forme des paragraphes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Mise en forme des paragraphes{#paragraph-formatting}

Les commandes de formatage des paragraphes suivants sont prises en charge.

<table id="table_5DD044E1C0614A29A2413557DF57197D"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Commander </p> </th> 
   <th class="entry"> <p>Description </p> </th> 
   <th class="entry"> <p>Remarques </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>Réinitialiser la mise en forme des paragraphes par défaut. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \Ql </span> </td> 
   <td> <p>Texte aligné à gauche. </p> </td> 
   <td> <p>Faire défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \Qr </span> </td> 
   <td> <p>Aligner le texte à droite. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \Qc </span> </td> 
   <td> <p>Centre le texte horizontalement. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>Justifie le texte horizontalement. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastQl </span> </td> 
   <td> <p>Aligne la dernière ligne d’un paragraphe à gauche. </p> </td> 
   <td> <p>Faire défaut; <span class="codeph"> textPs= </span> only ; ignoré si <span class="codeph"> \qj n’est </span>pas actif. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastQR </span> </td> 
   <td> <p>Aligne à droite la dernière ligne d’un paragraphe justifié. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only ; ignoré si <span class="codeph"> \qj n’est </span> pas actif. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastQc </span> </td> 
   <td> <p>Centre la dernière ligne d’un paragraphe justifié. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only ; ignoré si <span class="codeph"> \qj n’est </span>pas actif. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>Sustifier (étirer) la dernière ligne d’un paragraphe justifié. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only ; ignoré si <span class="codeph"> \qj n’est </span>pas actif. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>Retrait de la première ligne. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>Retrait à gauche. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>Retrait à droite. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>Espace entre les lignes. </p> </td> 
   <td> <p>0 (par défaut) pour l’interligne automatique ; valeurs positives pour n’utiliser la valeur que si elle est supérieure à l’interligne par défaut ; valeur négative pour forcer l’espacement. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>Interligne avec indicateur multiple. </p> </td> 
   <td> <p>Défini sur 0 (par défaut) si <span class="codeph"> \sl </span> est en twips, sur 1 si <span class="codeph"> \sl </span> est en multiples de l’espacement par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>Espace supplémentaire avant le paragraphe. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> text= </span>applique \sb <span class="codeph"> au premier paragraphe de la zone de texte, ce </span> qui n’est <span class="codeph"> pas le cas de textPs=</span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>Espace supplémentaire après le paragraphe. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> text= </span> applique \sa <span class="codeph"> au dernier paragraphe de la zone de texte, ce </span> qui n’est <span class="codeph"> pas le cas de textPs=</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>
