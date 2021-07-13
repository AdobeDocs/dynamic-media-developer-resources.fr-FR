---
description: Sélectionnez l’objet par emplacement de pixel.
solution: Experience Manager
title: sel
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# sel{#sel}

Sélectionnez l’objet par emplacement de pixel.

` sel= *``*, *``*[, *`xylevel`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y  </span> </p> </td> 
  <td class="stentry"> <p>Sélectionnez les coordonnées de l’emplacement en pixels (int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> niveau </span> </p> </td> 
  <td class="stentry"> <p>Au niveau du groupe (int). </p> </td> 
 </tr> 
</table>

Sélectionne le groupe ou l’objet aux coordonnées de pixel spécifiées par *`x, y`* et lance un nouveau MSS. Si aucun objet sélectionnable n’est à l’emplacement de sélection ou si l’emplacement de sélection n’est pas valide, l’action spécifiée par `attribute::OnFailSel` est exécutée.

*`level`* indique s’il faut sélectionner le groupe le plus éloigné ou accéder à un groupe ou à un objet imbriqué. Si *`level`* n’est pas spécifié, le groupe le plus éloigné est sélectionné. Définissez cette variable sur 1 pour sélectionner un niveau de groupe sous le groupe le plus éloigné. Définissez cette variable sur un nombre élevé (99, par exemple) pour sélectionner l’objet ou le groupe le plus sélectionnable.

## Propriétés {#section-8f27e84d88734a62a5e398e0c9972bdc}

la commande Sélection; Délimiteur MSS. La sélection d’objet est persistante jusqu’à ce qu’un autre objet soit sélectionné, soit avec `obj=` ou `sel=`.

*`x, y`* doit se trouver dans la plage 0, 0 (coin supérieur gauche de l’image) à  *`wid`*-1,  *`hei`*-1 (coin inférieur, coin droit de l’image), où  *`wid`* et  *`hei`* correspond à la taille de l’affichage de la vignette non mise à l’échelle.

Si spécifié, *`level`* doit être supérieur ou égal à 0.

## Par défaut {#section-e13c705a3e76468894b4ec190ed8a893}

Aucun pour *`x, y`*. *`level`* La valeur par défaut est 0.

## Voir aussi {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
