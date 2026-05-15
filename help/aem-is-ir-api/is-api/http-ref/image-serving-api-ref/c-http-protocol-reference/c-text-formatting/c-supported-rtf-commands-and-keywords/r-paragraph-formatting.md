---
description: Les commandes de formatage de paragraphe suivantes sont prises en charge.
solution: Experience Manager
title: Formatage des paragraphes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
TQID: 'https://experienceleague.adobe.com/bksi7t36irm8XQqI0LtJl3kNaSCZANRzbCKf80o-eNM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

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
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>Réinitialise la mise en forme des paragraphes à la valeur par défaut. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>Alignement à gauche du texte. </p> </td> 
   <td> <p>Valeur par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>Alignement à droite du texte. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>Centrer le texte horizontalement. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>Justifier le texte horizontalement. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>Aligner à gauche la dernière ligne d’un paragraphe. </p> </td> 
   <td> <p>Valeur par défaut ; <span class="codeph"> textPs= </span> uniquement ; ignoré si <span class="codeph"> \qj </span>n’est pas actif. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>Aligner à droite la dernière ligne d’un paragraphe justifié. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> uniquement ; ignoré si <span class="codeph"> \qj </span> n’est pas actif. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>Centrer la dernière ligne d’un paragraphe justifié. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> uniquement ; ignoré si <span class="codeph"> \qj </span>n’est pas actif. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>Étendre la dernière ligne d’un paragraphe justifié. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> uniquement ; ignoré si <span class="codeph"> \qj </span>n’est pas actif. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>Retrait de la première ligne. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> uniquement. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>Retrait à gauche. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> uniquement. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>Retrait à droite. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> uniquement. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>Espace entre les lignes. </p> </td> 
   <td> <p>0 (par défaut) pour l’espacement automatique des lignes ; valeurs positives pour utiliser uniquement la valeur si elle est supérieure à l’espacement par défaut ; valeur négative pour forcer l’espacement. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>Espacement des lignes de plusieurs indicateurs. </p> </td> 
   <td> <p>Définissez cette valeur sur 0 (valeur par défaut) si <span class="codeph"> \sl </span> est exprimé en twips, sur 1 si <span class="codeph"> \sl </span> est exprimé en multiples de l’espacement par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>Espace supplémentaire avant le paragraphe. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span>applique <span class="codeph"> \sb </span> au premier paragraphe de la zone de texte, <span class="codeph"> textPs= </span> ne l’applique pas. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>Espace supplémentaire après le paragraphe. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span> s’applique <span class="codeph"> \sa </span> au dernier paragraphe de la zone de texte, <span class="codeph"> textPs= </span> ne s’applique pas. </p> </td> 
  </tr> 
 </tbody> 
</table>
