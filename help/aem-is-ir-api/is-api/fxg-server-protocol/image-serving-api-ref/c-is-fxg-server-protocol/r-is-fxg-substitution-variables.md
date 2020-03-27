---
description: Les variables de substitution sont utilisées pour transférer des valeurs de l’URL de requête vers des modèles FXG stockés sur le serveur.
seo-description: Les variables de substitution sont utilisées pour transférer des valeurs de l’URL de requête vers des modèles FXG stockés sur le serveur.
seo-title: Variables de substitution
solution: Experience Manager
title: Variables de substitution
topic: Scene7 Image Serving - Image Rendering API
uuid: 87cd9594-ba3b-429d-aa57-399902ef3abe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Variables de substitution{#substitution-variables}

Les variables de substitution sont utilisées pour transférer des valeurs de l’URL de requête vers des modèles FXG stockés sur le serveur.

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span></span> </p> </td> 
  <td class="stentry"> <p>Nom de variable. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valeur </span></span> </p> </td> 
  <td class="stentry"> <p>Valeur à laquelle la variable doit être définie (chaîne). </p> </td> 
 </tr> 
</table>

* Les définitions de variable et les références peuvent se produire dans la partie  de l’URL de requête.
* Les variables sont définies comme ci-dessus, comme les autres commandes IS ; le caractère &quot;$&quot; en tête identifie la commande comme une définition de variable.
* Le nom de variable ` *`var`*` est sensible à la casse et peut se composer de n’importe quelle combinaison de lettres, de chiffres, de &quot;-&quot; et de &quot;_&quot;.
* La valeur importante doit être codée en URL à un seul passage pour une transmission HTTP sécurisée.

