---
title: Introduction
description: Ce document décrit le protocole HTTP pour le rendu d’images Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
TQID: 'https://experienceleague.adobe.com/I21iWFmYP0Vwunf3evtnLAr3tslHOsTOB0sGWG6l-bc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 387
ht-degree: 0%

---

# Introduction{#introduction}

Ce document décrit le protocole HTTP pour le rendu d’images Dynamic Media.

Seuls les aspects du protocole accessibles au public sont décrits. Le serveur peut prendre en charge des commandes supplémentaires qui sont réservées à l’utilisation par le logiciel client Dynamic Media.

**Audience ciblée**

Ce document est destiné aux programmeurs et aux développeurs de sites web expérimentés qui souhaitent utiliser le rendu d’images Dynamic Media pour un site web ou une application personnalisée.

Le lecteur est supposé être familiarisé avec la création d’images et le rendu d’images Dynamic Media, les normes et conventions générales du protocole HTTP et la terminologie de base de l’imagerie.

**Conventions de document**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>littéral </p> </td> 
  <td class="stentry"> <p>Dans les sections de syntaxe, le texte non italique est littéral ; il ne s’applique pas aux espaces et aux symboles [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'littéral' </p> </td> 
  <td class="stentry"> <p>Dans les sections descriptives, le texte non italique entre guillemets simples est littéral. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> du paramètre <span class="varname"> </p> </td> 
  <td class="stentry"> <p>L’italique indique une variable ou un paramètre à remplacer par une valeur réelle. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe 'attribute::' fait référence à un attribut de catalogue d'images. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de 'catalog::' fait référence à un champ de données de catalogue de matériaux. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe « icc:: » fait référence à un champ de la carte de profil colorimétrique ICC. </p> </td> 
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
  <td class="stentry"> <p>Un nom précédé de 'default::' fait référence à un attribut du catalogue d’images par défaut. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> vignette::Item </span> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe 'vignette::' fait référence à un champ de la carte des vignettes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> facultatif </span> ] </p> </td> 
  <td class="stentry"> <p>Les éléments de syntaxe facultatifs sont placés entre crochets. </p> </td> 
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
  <td class="stentry"> <p>Les éléments de syntaxe au sein du groupe peuvent être répétés une ou plusieurs fois. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>espace blanc </p> </td> 
  <td class="stentry"> <p>Les espaces (espaces ou tabulations) ne sont pas autorisés dans les requêtes HTTP. Ce document utilise parfois des espaces blancs entre les éléments syntaxiques pour des raisons de clarté uniquement. </p> </td> 
 </tr> 
</table>

**Termes courants**

**&#x200B; *`MSS`* &#x200B;** Segment de spécification de matière : ensemble d&#39;attributs de matière entre deux commandes de sélection dans la demande.

**&#x200B; *`vignette`* &#x200B;** Image préparée dans la création d’images Dynamic Media en vue d’être utilisée avec le rendu d’image.
