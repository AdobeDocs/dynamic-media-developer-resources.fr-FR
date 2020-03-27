---
description: Ce décrit le protocole HTTP pour le rendu des images Scene7.
seo-description: Ce décrit le protocole HTTP pour le rendu des images Scene7.
seo-title: Introduction
solution: Experience Manager
title: Introduction
topic: Scene7 Image Serving - Image Rendering API
uuid: d709f1d2-e7cc-4e9f-b039-aa333e517cbb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Introduction{#introduction}

Ce décrit le protocole HTTP pour le rendu des images Scene7.

Seuls les aspects du protocole accessibles au public sont décrits. Le serveur peut prendre en charge d’autres commandes réservées au logiciel client Scene7.

**prévu**

Ce document est destiné aux développeurs de sites Web et aux programmeurs chevronnés qui souhaitent exploiter le rendu d’image Scene7 pour un site Web ou une application personnalisée.

On suppose que le lecteur connaît bien Scene7 Image Authoring and Image Rendering, les normes et conventions générales relatives au protocole HTTP et la terminologie de base de l’imagerie.

**Conventions de**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>littéral </p> </td> 
  <td class="stentry"> <p>Dans les sections de syntaxe, le texte non italique est littéral ; cela ne s’applique pas à l’espace blanc et aux symboles [ ] { }| *. </p> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> attribut:Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de 'attribute::' fait référence à un attribut de catalogue d’images. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalogue::Elément </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de "catalog::" fait référence à un champ de données de catalogue de matières. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de "icc::" fait référence à un champ de la carte de de couleurs ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro:Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de "macro::" fait référence à un champ de la table de définition de macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ensemble de règles:Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe "ruleSet::" fait référence à un élément d’un jeu de règles de prétraitement d’URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de "default::" fait référence à un attribut du catalogue d’images par défaut. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> vignette:Item </span> </td> 
  <td class="stentry"> <p>Un nom précédé de "vignette:" fait référence à un champ de la carte de vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>Les éléments de syntaxe facultatifs sont placés entre crochets. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>L’élément de syntaxe facultatif peut être répété aucune ou plusieurs fois. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> élément2 </span> </p> </td> 
  <td class="stentry"> <p>Une barre verticale indique que l’élément de syntaxe unique à gauche ou l’élément à droite peut être utilisé. Vous devez sélectionner exactement un élément. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> groupe </span> } </p> </td> 
  <td class="stentry"> <p>Les accolades sont utilisées pour regrouper les éléments de syntaxe. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> groupe </span> } </p> </td> 
  <td class="stentry"> <p>Les éléments de syntaxe du groupe peuvent être répétés une ou plusieurs fois. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>espace blanc </p> </td> 
  <td class="stentry"> <p>Les espaces (espaces ou onglets) ne sont pas autorisés dans les requêtes HTTP. Ce utilise occasionnellement l’espace blanc entre les éléments syntaxiques à des fins de clarté seulement. </p> </td> 
 </tr> 
</table>

**Termes communs**

** *`MSS`* ** Segment de spécification du matériau : un ensemble d’attributs matériels entre deux commandes de sélection dans la requête.

** *`vignette`* ** Image préparée dans Scene7 Image Authoring pour être utilisée avec le rendu d’image.
