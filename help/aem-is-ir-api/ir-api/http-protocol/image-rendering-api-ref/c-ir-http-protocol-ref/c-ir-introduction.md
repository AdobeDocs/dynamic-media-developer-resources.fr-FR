---
title: Introduction
description: Ce document décrit le protocole HTTP pour le rendu d’image Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---

# Introduction{#introduction}

Ce document décrit le protocole HTTP pour le rendu d’image Dynamic Media.

Seuls les aspects du protocole accessibles au public sont décrits. Le serveur peut prendre en charge des commandes supplémentaires, réservées à l’utilisation par le logiciel client Dynamic Media.

**Audience prévue**

Ce document est destiné aux programmeurs expérimentés et aux développeurs de sites web qui souhaitent utiliser le rendu d’image Dynamic Media pour un site web ou une application personnalisée.

On suppose que le lecteur connaît bien la création et le rendu d’images Dynamic Media, les normes et conventions générales du protocole HTTP et la terminologie de base de l’imagerie.

**Conventions relatives aux documents**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>littéral </p> </td> 
  <td class="stentry"> <p>Dans les sections de syntaxe, le texte non italique est littéral ; il ne s’applique pas à l’espace blanc et aux symboles [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'littéral' </p> </td> 
  <td class="stentry"> <p>Dans les sections descriptives, le texte non italique entre guillemets simples est littéral. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> paramètre </span> </p> </td> 
  <td class="stentry"> <p>Les caractères italiques indiquent une variable ou un paramètre à remplacer par une valeur réelle. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe 'attribute::' fait référence à un attribut du catalogue d’images. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe "catalog:" fait référence à un champ de données de catalogue matériel. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe "icc:" fait référence à un champ de la carte des profils de couleurs ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe 'macro:' fait référence à un champ de la table de définition des macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleSet::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe "ruleSet:" fait référence à un élément d’un jeu de règles de prétraitement d’URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe "default:" fait référence à un attribut du catalogue d’images par défaut. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> vignette : élément </span> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe 'vignette:' fait référence à un champ de la vignette. </p> </td> 
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
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </p> </td> 
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
  <td class="stentry"> <p>espace blanc </p> </td> 
  <td class="stentry"> <p>Les espaces (espaces ou onglets) ne sont pas autorisés dans les requêtes HTTP. Ce document utilise parfois des espaces blancs entre les éléments syntaxiques uniquement à des fins de clarté. </p> </td> 
 </tr> 
</table>

**Termes communs**

** *`MSS`* ** Segment de spécification de matériel : un ensemble d’attributs matériels entre deux commandes de sélection dans la requête.

** *`vignette`* ** Image préparée dans Dynamic Media Image Authoring pour une utilisation avec le rendu d’image.
