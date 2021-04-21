---
description: Mise à l’échelle des images basée sur la résolution. Met l’image à l’échelle avec la résolution demandée.
solution: Experience Manager
title: res
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 1%

---


# res{#res}

Mise à l’échelle des images basée sur la résolution. Met l’image à l’échelle avec la résolution demandée.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Résolution des cibles ; généralement en pixels par pouce (réel). </p> </td> 
 </tr> 
</table>

Le facteur d&#39;échelle est calculé en divisant *`val`* par `catalog::Resolution`. Notez que cette commande n’affecte pas la résolution d’impression de l’image de réponse.

Pour utiliser cette fonctionnalité, la résolution des images source d’origine doit être connue et définie dans `catalog::Resolution`. Selon l&#39;application, les unités de résolution peuvent varier. Pour les textures 2D répétables ou les nuances de matériau, telles que les papiers peints ou les tissus, la résolution peut être exprimée en pixels/pouce ou en pixels/mm. Les photos et les cartes aériennes peuvent être mieux desservies par les pixels/mille ou les pixels/km. Dans tous les cas, les unités utilisées pour `catalog::Resolution` doivent être identiques à celles utilisées pour `res=`.

En plus d&#39;obtenir des images à des résolutions précises, `res=` peut également être utilisé pour combiner plusieurs images à la même résolution, de sorte que les éléments visibles dans ces images soient en proportion exacte les uns des autres.

>[!NOTE]
>
>Normalement, une image composite est redimensionnée à la taille de vue de la cible (spécifiée par `wid=`, `hei=` ou `attribute::DefaultPix`) avant d’être renvoyée au client. Pour éviter ce redimensionnement et obtenir une image avec la résolution exacte spécifiée par `res=`, il peut être nécessaire de désactiver la mise à l’échelle des vues en spécifiant explicitement `scl=1`. Cela indique au serveur de recadrer l’image composite selon la taille de la vue de la cible plutôt que de la redimensionner.

## Propriétés {#section-fdbd16e59cff4952a3717146bc91412e}

Attribut image/masque source. Ignoré par les calques non associés à une image ou un masque source. Appliqué au calque 0 est spécifié pour `layer=comp`. Ignoré si `scale=` ou `size=` est spécifié pour le même calque.

## Par défaut {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

Si elle n’est pas spécifiée, `scale=` ou `size=` détermine le facteur d’échelle ou, si aucune de ces deux valeurs n’est spécifiée, l’image est utilisée sans mise à l’échelle.

## Exemple {#section-eb06f333e08e4247971fb1b18922597b}

Récupérez une image de texture à une résolution d’objet de 12 pixels/pouce à utiliser avec le rendu d’image ou la création d’images. Nous spécifions le format PNG sans perte et une meilleure qualité de rééchantillonnage pour une qualité optimale,

` http:// *`server`*/myTexture?res=12&fmt=png&resMode=sharp`

## Voir aussi {#section-1f8a8f11772e493ca803c4511f397a11}

[catalogue ::Résolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) ,  [attribut::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
