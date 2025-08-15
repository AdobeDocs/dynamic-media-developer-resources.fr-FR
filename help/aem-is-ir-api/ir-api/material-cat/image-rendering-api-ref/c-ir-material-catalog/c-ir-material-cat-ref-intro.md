---
description: Ce document décrit le catalogue de matériaux pour Dynamic Media rendu d’images.
solution: Experience Manager
title: Introduction
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1cdb9c45-329d-44df-92c3-8cba5b2b1339
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# Introduction{#introduction}

Ce document décrit le catalogue de matériaux pour le rendu d’images Dynamic Media.

**Audience ciblée**

Ce document est destiné aux programmeurs expérimentés et aux développeurs de sites Web qui souhaitent tirer parti de Dynamic Media Image Rendering pour un site Web ou une application personnalisée.

Il est supposé que le lecteur est familier avec Dynamic Media la création d’images et le rendu d’images, les normes et conventions générales du protocole HTTP et la terminologie de base de l’imagerie.

**Conventions du document**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Littéral </p> </td> 
  <td class="stentry"> <p>Dans les sections de syntaxe, le texte non italique est littéral ; Ceci ne s’applique pas aux espaces blancs et aux symboles [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>« littéral » </p> </td> 
  <td class="stentry"> <p>Dans les sections descriptives, le texte non italique dans les guillemets simples est littéral. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> du paramètre </span> </p> </td> 
  <td class="stentry"> <p>L’italique indique une variable ou un paramètre à remplacer par une valeur réelle. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe 'attribute::' fait référence à un attribut de catalogue d'images. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> catalogue ::Article </span> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe « catalog :: » fait référence à un champ de données de catalogue de matériaux. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc ::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe « icc :: » fait référence à un champ de la carte de profils de couleurs ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro ::Élément </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe « macro :: » fait référence à un champ de la table de définition des macros. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de 'ruleset::' fait référence à un élément dans un ensemble de règles de pré-traitement d'URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de 'default::' fait référence à un attribut du catalogue d’images par défaut. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> vignette::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe 'vignette ::' fait référence à un champ de la carte des vignettes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">[ facultatif </span> ] </p> </td> 
  <td class="stentry"> <p>Les éléments de syntaxe facultatifs sont compris entre crochets. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> facultatif </span> ] </p> </td> 
  <td class="stentry"> <p>L’élément de syntaxe facultatif ne peut être répété ni une ou plusieurs fois. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> élément1 </span>| <span class="varname"> élément2 </span> </p> </td> 
  <td class="stentry"> <p>Une barre verticale indique que l’élément de syntaxe unique à gauche ou l’élément à droite peut être utilisé. Un seul élément doit être sélectionné. </p> </td> 
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
  <td class="stentry"> <p>Espace blanc. </p> </td> 
  <td class="stentry"> <p>Les espaces blancs (espaces ou tabulations) ne sont pas autorisés dans les requêtes HTTP. Ce document utilise parfois des espaces entre les éléments syntaxiques uniquement pour plus de clarté. </p> </td> 
 </tr> 
</table>
