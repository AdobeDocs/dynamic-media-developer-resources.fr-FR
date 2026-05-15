---
description: Ce document utilise les conventions suivantes.
solution: Experience Manager
title: Conventions de document
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e93de3fa-dde1-4d79-93aa-9ad800840cfc
TQID: 'https://experienceleague.adobe.com/NuClwLkfN7-tuVMYcn610qL7-bQOQbVz940uTPAxk-g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 283
ht-degree: 0%

---

# Conventions de document{#document-conventions}

Ce document utilise les conventions suivantes.

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>littéral </p> </td> 
  <td class="stentry"> <p>Dans les sections de syntaxe, le texte non italique est littéral. Cette règle ne s’applique pas aux espaces et aux symboles [ ] { } | *. </p> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> command= </span> </p> </td> 
  <td class="stentry"> <p>Un nom avec un signe de fin « = » fait référence à une commande de protocole HTTP de diffusion d’images. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de <span class="codeph"> attribut : </span> fait référence à un attribut de catalogue d’images. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé du préfixe <span class="codeph"> catalogue : </span> fait référence à un champ de données de catalogue d’images. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé <span class="codeph"> icc : </span> fait référence à un champ de la carte de profil colorimétrique ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> font::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé d’<span class="codeph"> police : </span> fait référence à un champ du mappage des polices. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro : élément </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de <span class="codeph"> macro : </span> fait référence à un champ de la table de définition de la macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé <span class="codeph">’un jeu de règles : </span> fait référence à un élément dans un jeu de règles de pré-traitement des URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item </span> </p> </td> 
  <td class="stentry"> <p>Un nom précédé de <span class="codeph"> valeur par défaut : </span> fait référence à un attribut du catalogue d’images par défaut. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [ <span class="varname"> facultatif </span>] </span> </p> </td> 
  <td class="stentry"> <p>Les éléments de syntaxe facultatifs sont placés entre crochets. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[ <span class="varname"> facultatif </span>] </span> </p> </td> 
  <td class="stentry"> <p>L’élément de syntaxe </span> facultatif <span class="varname"> peut être répété une ou plusieurs fois. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </span> </p> </td> 
  <td class="stentry"> <p>Une barre verticale indique que l’élément de syntaxe unique à gauche ou l’élément à droite peut être utilisé. Un seul élément doit être sélectionné. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> { <span class="varname"> groupe </span>} </span> </p> </td> 
  <td class="stentry"> <p>Les accolades sont utilisées pour regrouper les éléments de syntaxe. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{ <span class="varname"> groupe </span>} </span> </p> </td> 
  <td class="stentry"> <p>Les éléments de syntaxe du groupe peuvent être répétés une ou plusieurs fois. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>espace blanc </p> </td> 
  <td class="stentry"> <p>Les espaces (espaces ou tabulations) ne sont pas autorisés dans les requêtes HTTP. Ce document utilise parfois des espaces blancs entre les éléments syntaxiques pour des raisons de clarté uniquement. </p> </td> 
 </tr> 
</table>
