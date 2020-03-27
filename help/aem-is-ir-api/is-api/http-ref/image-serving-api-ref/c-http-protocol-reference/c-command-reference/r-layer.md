---
description: Sélectionnez Calque. Sélectionne un calque et  un nouveau segment de définition de calque dans la séquence de commandes.
seo-description: Sélectionnez Calque. Sélectionne un calque et  un nouveau segment de définition de calque dans la séquence de commandes.
seo-title: calque
solution: Experience Manager
title: calque
topic: Scene7 Image Serving - Image Rendering API
uuid: 882309b3-51d7-477e-bd09-068ce9e55eb5
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# layer{#layer}

Sélectionnez Calque. Sélectionne un calque et  un nouveau segment de définition de calque dans la séquence de commandes.

`layer= *``*|comp[, *`nname`*]`

`layer= *`nom`*`

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
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nom</span></span> </p></td> 
  <td class="stentry"> <p>Nom de couche. </p></td> 
 </tr> 
</table>

Toutes les commandes du segment de calque sont appliquées au calque spécifié. Un segment de calque se termine par la commande suivante `layer=` ou `effect=` ou par la fin de la requête.

Spécifiez `layer=comp` la sélection de l’image composite (ou du , pour certaines commandes).

Le numéro de calque spécifie l’ordre z du calque. Les calques à numéro supérieur sont placés au-dessus des calques à numéro inférieur.

Les numéros de calque ne doivent pas nécessairement être consécutifs. La couche 0 est requise.

Un nom peut être attribué à un calque avec la variante de commande `layer= *``*, *`nname`*` . Une fois qu’un calque nommé est défini, il peut être référencé par ` layer= *`son nom`*`, sans qu’il faille connaître le numéro du calque. Plusieurs noms peuvent être attribués à la même couche, à l’aide de plusieurs commandes `layer= *``*, *`nname`*` .

>[!NOTE]
>
>La couche 0 détermine la taille globale de la zone de travail de composition. Toutes les parties de calques situées en dehors des limites du calque 0 sont rognées lorsque le composite est créé.

## Propriétés {#section-499963ee52c14f2898f0d0f90c1d01be}

Calque, commande. Les références aux variables de substitution ne sont pas prises en charge dans `layer=`.

`comp` n’est pas autorisée en tant que *`name`* chaîne. Une erreur est renvoyée si la même *`name`* est affectée à plusieurs calques ou si un calque est référencé par *`name`* lequel il n’a pas été défini précédemment.

## Par défaut {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. De nombreuses commandes et attributs s’appliquent au calque 0 si `layer=comp`.

## Cas particuliers {#section-e087cb2e3562473e8d391abfa3b9489f}

* Si le même nom est associé à plusieurs calques (par exemple : `layer=1,image&layer=2,image`), une erreur se produit.
* Si le même nom est mappé sur un calque unique plusieurs fois (par exemple : `layer=1,image&layer=1,image`), la portée est définie comme d’habitude, sans erreurs.
* Plusieurs noms pour le même calque sont pris en charge.

   Vous pouvez utiliser l’un ou l’autre nom pour référencer le calque (par exemple : `layer=1,image&layer=1,picture`).
* Si un nom référencé n’est jamais associé à un numéro de calque (par exemple : `layer=1,image&layer=picture`), une erreur se produit.
* Les variables de substitution ne sont pas prises en charge dans les modificateurs de calque (par exemple : `layer=$image$`).

   Cela s’applique à toutes les permutations, non seulement aux noms de calque, mais aussi aux modificateurs de calque en général.

* Toutes les règles de fusion et de remplacement doivent fonctionner exactement comme lorsque le même calque est référencé dans plusieurs sources (enregistrements de catalogue de modificateurs de requête, de pré ou post, macros, etc.).

## Exemple {#section-cc40de6a0a754178aa752601539c815b}

Voir les exemples dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
