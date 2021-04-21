---
description: Les variables de substitution sont utilisées pour transférer des valeurs de l’URL de requête vers des modèles FXG stockés sur le serveur.
solution: Experience Manager
title: Variables de substitution
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# Variables de substitution{#substitution-variables}

Les variables de substitution sont utilisées pour transférer des valeurs de l’URL de requête vers des modèles FXG stockés sur le serveur.

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nom de variable. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur à laquelle la variable doit être définie (chaîne). </p> </td> 
 </tr> 
</table>

* Les définitions de variable et les références peuvent se trouver dans la partie requête de l’URL de demande.
* Les variables sont définies comme ci-dessus, comme les autres commandes IS ; l&#39;en-tête &#39;$&#39; identifie la commande comme une définition de variable.
* Le nom de variable `*`var`*` est sensible à la casse et peut être composé de toute combinaison de lettres, de chiffres, de &#39;-&#39; et de &#39;_&#39;.
* La valeur importante doit être codée en URL à un seul passage pour une transmission HTTP sécurisée.

