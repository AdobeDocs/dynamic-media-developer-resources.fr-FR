---
description: Sélectionnez Calque. Sélectionne un calque et début un nouveau segment de définition de calque dans la séquence de commandes.
solution: Experience Manager
title: calque
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 1%

---


# layer{#layer}

Sélectionnez Calque. Sélectionne un calque et début un nouveau segment de définition de calque dans la séquence de commandes.

`layer= *``*|comp[, *`nom`*]`

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
  <td class="stentry"> <p>Nom de couche. </p></td> 
 </tr> 
</table>

Toutes les commandes du segment de calque sont appliquées au calque spécifié. Un segment de calque est terminé par la prochaine commande `layer=` ou `effect=` ou par la fin de la requête.

Spécifiez `layer=comp` pour sélectionner l’image composite (ou la vue, pour certaines commandes).

Le numéro de calque spécifie effectivement l’ordre z du calque. Les calques à numérotation supérieure sont placés au-dessus des calques à numérotation inférieure.

Les numéros de calque ne doivent pas nécessairement être consécutifs. La couche 0 est requise.

Un nom peut être attribué à un calque avec la variante de commande `layer= *`n`*, *`name`*`. Une fois qu’un calque nommé est défini, il peut être référencé avec ` layer= *`name`*`, sans connaître le numéro du calque. Plusieurs noms peuvent être attribués à la même couche, en utilisant plusieurs commandes `layer= *`n`*, *`name`*`.

>[!NOTE]
>
>La couche 0 détermine la taille globale de la trame de composition. Toutes les parties des calques qui se trouvent en dehors des limites du calque 0 sont rognées lorsque le composite est créé.

## Propriétés {#section-499963ee52c14f2898f0d0f90c1d01be}

Calque, commande. Les références de variable de substitution ne sont pas prises en charge dans `layer=`.

`comp` n’est pas autorisée en tant que  *`name`* chaîne. Une erreur est renvoyée si le même *`name`* est affecté à plusieurs calques ou si un calque est référencé par *`name`* qui n&#39;a pas été défini précédemment.

## Par défaut {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. De nombreuses commandes et attributs s&#39;appliquent à la couche 0 si `layer=comp`.

## Cas particuliers {#section-e087cb2e3562473e8d391abfa3b9489f}

* Si le même nom est associé à plusieurs calques (par exemple : `layer=1,image&layer=2,image`), une erreur se produit.
* Si le même nom est mappé sur un seul calque plusieurs fois (par exemple : `layer=1,image&layer=1,image`), la portée est définie comme d’habitude, sans erreurs.
* Plusieurs noms pour un même calque sont pris en charge.

   Vous pouvez utiliser l’un ou l’autre nom pour référencer le calque (par exemple : `layer=1,image&layer=1,picture`).
* Si un nom référencé n’est jamais associé à un numéro de calque (par exemple : `layer=1,image&layer=picture`), une erreur se produit.
* Les variables de substitution ne sont pas prises en charge dans les modificateurs de calque (par exemple : `layer=$image$`).

   Cela s&#39;applique à toutes les permutations, non seulement aux noms de calque mais aux modificateurs de calque en général.

* Toutes les règles de fusion et de remplacement doivent fonctionner exactement comme lorsque la même couche est référencée dans plusieurs sources (enregistrements de catalogue de modificateurs de requête, de pré-modification ou de post, macros, etc.).

## Exemple {#section-cc40de6a0a754178aa752601539c815b}

Voir les exemples dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
