---
description: Les variables de substitution sont utilisées pour transférer des valeurs de l’URL de demande vers des modèles FXG stockés sur le serveur.
solution: Experience Manager
title: Variables de substitution
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# Variables de substitution{#substitution-variables}

Les variables de substitution sont utilisées pour transférer des valeurs de l’URL de demande vers des modèles FXG stockés sur le serveur.

` $ *`var`*= *`value`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Nom de la variable. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur à laquelle la variable doit être définie (chaîne). </p> </td> 
 </tr> 
</table>

* Les définitions et références de variables peuvent se produire dans la partie requête de l’URL de requête.
* Les variables sont définies comme ci-dessus, comme les autres commandes IS ; le &quot;$&quot; au début identifie la commande comme une définition de variable.
* Le nom de variable `*`var`*` est sensible à la casse et peut se composer de n’importe quelle combinaison de lettres, de nombres, de &quot;-&quot; et de &quot;_&quot;.
* La valeur importante doit être codée en URL à un seul passage pour une transmission HTTP sécurisée.
