---
title: layer
description: Sélectionnez Calque. Sélectionne un calque et lance un nouveau segment de définition de calque dans la séquence de commandes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# layer{#layer}

Sélectionnez Calque. Sélectionne un calque et lance un nouveau segment de définition de calque dans la séquence de commandes.

`layer= *`n`*|comp[, *`name`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>Nombre de calques à sélectionner (0 ou plus int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>Sélectionnez l’image composite. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>Nom du calque. </p></td> 
 </tr> 
</table>

Toutes les commandes du segment de calque sont appliquées au calque spécifié. Un segment de calque est arrêté par la commande `layer=` ou `effect=` suivante ou la fin de la requête.

Spécifiez `layer=comp` pour sélectionner l’image composite (ou l’affichage, pour certaines commandes).

Le numéro de calque spécifie l’ordre z du calque. Les calques à numéro supérieur sont placés au-dessus des calques à numéro inférieur.

Les numéros de calque ne doivent pas nécessairement être consécutifs. La couche 0 est requise.

Un nom peut être attribué à un calque avec la variante de commande `layer= *`n`*, *`name`*` . Une fois défini, un calque nommé peut être référencé avec ` layer= *`name`*`, sans avoir à connaître le numéro du calque. Plusieurs noms peuvent être attribués à la même couche à l’aide de plusieurs commandes `layer= *`n`*, *`name`*`.

>[!NOTE]
>
>Le calque 0 détermine la taille globale du canevas de composition. Toutes les parties des calques situés en dehors des limites de la couche 0 sont rognées lors de la création du composite.

## Propriétés {#section-499963ee52c14f2898f0d0f90c1d01be}

Couche, commande. Les références de variables de substitution ne sont pas prises en charge dans `layer=`.

`comp` n’est pas autorisé en tant que chaîne *`name`*. Une erreur est renvoyée si le même *`name`* est affecté à plusieurs calques ou si un calque est référencé par *`name`* qui n’a pas été défini précédemment.

## Par défaut {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. De nombreuses commandes et attributs s’appliquent à la couche 0 si `layer=comp`.

## Cas particuliers {#section-e087cb2e3562473e8d391abfa3b9489f}

* Si le même nom est mappé à plusieurs calques (par exemple : `layer=1,image&layer=2,image`), une erreur se produit.
* Si le même nom est mappé plusieurs fois à un seul calque (par exemple : `layer=1,image&layer=1,image`), la portée est définie comme d’habitude, sans erreur.
* Plusieurs noms pour le même calque sont pris en charge.

  N’importe quel nom peut être utilisé pour référencer le calque (par exemple : `layer=1,image&layer=1,picture`).
* Si un nom référencé n’est jamais mappé à un numéro de calque (par exemple : `layer=1,image&layer=picture`), une erreur se produit.
* Les variables de substitution ne sont pas prises en charge dans les modificateurs de calque (par exemple : `layer=$image$`).

  Cela s’applique à toutes les permutations, non seulement aux noms de calque, mais aussi aux modificateurs de calque en général.

* Toutes les règles de fusion et de remplacement doivent fonctionner exactement comme lorsqu’une même couche est référencée dans plusieurs sources (enregistrements de catalogue de modificateurs de requête, de pré-modification ou de publication, macros, etc.).

## Exemple {#section-cc40de6a0a754178aa752601539c815b}

Voir les exemples dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
