---
description: Ce document décrit le catalogue de matériaux pour le rendu d’image Dynamic Media.
solution: Experience Manager
title: Introduction
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Introduction{#introduction}

Ce document décrit le catalogue de matériaux pour le rendu d’image Dynamic Media.

**Audience prévue**

Ce document est destiné aux programmeurs expérimentés et aux développeurs de sites Web qui souhaitent exploiter le rendu d’image Dynamic Media pour un site Web ou une application personnalisée.

Il est supposé que le lecteur connaît bien la création et le rendu d’images Dynamic Media, les normes et conventions de protocole HTTP générales et la terminologie de base de l’imagerie.

**Conventions relatives aux documents**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Littéral </p> </td> 
  <td class="stentry"> <p>Dans les sections de syntaxe, le texte non italique est littéral ; cela ne s’applique pas à l’espace blanc et aux symboles [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'littéral' </p> </td> 
  <td class="stentry"> <p>Dans les sections descriptives, le texte non italique entre guillemets simples est littéral. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> paramètre </span> </p> </td> 
  <td class="stentry"> <p>Les italiques indiquent une variable ou un paramètre, à remplacer par une valeur réelle. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribut::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de "attribute::" fait référence à un attribut de catalogue d’images. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> catalogue : élément  </span> </td> 
  <td class="stentry"> <p>Un nom précédé de "catalog::" fait référence à un champ de données de catalogue de matières. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de "icc::" fait référence à un champ de la carte de profil de couleur ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de "macro::" fait référence à un champ de la table de définition de macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ensemble de règles ::Élément  </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de "rule eset::" fait référence à un élément d’un jeu de règles de prétraitement d’URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de "default::" fait référence à un attribut du catalogue d’images par défaut. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> vignette : élément  </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de "vignette :" fait référence à un champ de la carte de vignettes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> facultatif </span> ] </p> </td> 
  <td class="stentry"> <p>Les éléments de syntaxe facultatifs sont entourés de crochets. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> facultatif </span> ] </p> </td> 
  <td class="stentry"> <p>L’élément de syntaxe facultatif peut être répété aucune ou plusieurs fois. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1  </span>|  <span class="varname"> item2  </span> </p> </td> 
  <td class="stentry"> <p>Une barre verticale indique que l’élément de syntaxe unique à gauche ou l’élément à droite peut être utilisé. Vous devez sélectionner exactement un élément. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> groupe </span> } </p> </td> 
  <td class="stentry"> <p>Les accolades sont utilisées pour regrouper les éléments de syntaxe. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> groupe </span> } </p> </td> 
  <td class="stentry"> <p>Les éléments syntaxiques du groupe peuvent être répétés une ou plusieurs fois. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Espace blanc. </p> </td> 
  <td class="stentry"> <p>Les espaces blancs (espaces ou onglets) ne sont pas autorisés dans les requêtes HTTP. Ce document utilise occasionnellement un espace entre les éléments syntaxiques pour la clarté seulement. </p> </td> 
 </tr> 
</table>

