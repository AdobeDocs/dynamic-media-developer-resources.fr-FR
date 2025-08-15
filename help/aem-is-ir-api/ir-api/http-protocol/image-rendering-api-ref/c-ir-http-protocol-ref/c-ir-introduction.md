---
title: Introduction
description: Ce document décrit le protocole HTTP pour le rendu d’images Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Introduction{#introduction}

Ce document décrit le protocole HTTP pour le rendu d’images Dynamic Media.

Seuls les aspects du protocole accessibles au public sont décrits. Le serveur peut prendre en charge des commandes supplémentaires qui sont réservées à une utilisation par Dynamic Media logiciel client.

**Public visé**

Ce document est destiné aux programmeurs expérimentés et aux développeurs de sites Web qui souhaitent utiliser Dynamic Media Image Rendering pour un site Web ou une application personnalisée.

Il est supposé que le lecteur est familier avec Dynamic Media la création d’images et le rendu d’images, les normes et conventions générales du protocole HTTP et la terminologie de base de l’imagerie.

**Conventions du document**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>littéral </p> </td> 
  <td class="stentry"> <p>Dans les sections de syntaxe, le texte non italique est littéral ; Elle ne s’applique pas aux espaces blancs ni aux symboles [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'littéral' </p> </td> 
  <td class="stentry"> <p>Dans les sections descriptives, le texte non italique entre guillemets simples est littéral. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> du paramètre </span> </p> </td> 
  <td class="stentry"> <p>L’italique indique une variable ou un paramètre à remplacer par une valeur réelle. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribut ::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe 'attribute ::' fait référence à un attribut de catalogue d’images. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalogue ::Article </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe « catalog :: » fait référence à un champ de données de catalogue de matériaux. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc ::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe « icc :: » fait référence à un champ de la carte de profils de couleurs ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe 'macro::' fait référence à un champ du tableau de définition de macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de 'ruleset::' fait référence à un élément dans un ensemble de règles de pré-traitement d'URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe 'default ::' fait référence à un attribut du catalogue d’images par défaut. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> vignette ::Item </span> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe 'vignette ::' fait référence à un champ de la carte des vignettes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">[ facultatif </span> ] </p> </td> 
  <td class="stentry"> <p>Les éléments de syntaxe facultatifs sont compris entre crochets. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> facultatif </span> ] </p> </td> 
  <td class="stentry"> <p>L’élément de syntaxe facultatif peut être répété une ou plusieurs fois. </p> </td> 
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
  <td class="stentry"> <p>Les espaces blancs (espaces ou tabulations) ne sont pas autorisés dans les requêtes HTTP. Ce document utilise parfois des espaces entre les éléments syntaxiques uniquement pour plus de clarté. </p> </td> 
 </tr> 
</table>

**Termes courants**

**&#x200B; *`MSS`* &#x200B;** Segment de spécification de matière : ensemble d&#39;attributs de matière entre deux commandes de sélection dans la demande.

**&#x200B; *`vignette`* &#x200B;** Image préparée dans la création d’images Dynamic Media en vue d’être utilisée avec le rendu d’image.
