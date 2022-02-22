---
title: sel
description: Sélectionnez l’objet par emplacement de pixel.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# sel{#sel}

Sélectionnez l’objet par emplacement de pixel.

` sel= *`x`*, *`y`*[, *`level`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>Sélectionnez les coordonnées de l’emplacement en pixels (int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> niveau </span> </p> </td> 
  <td class="stentry"> <p>Au niveau du groupe (int). </p> </td> 
 </tr> 
</table>

Sélectionne le groupe ou l’objet aux coordonnées de pixel spécifiées par *`x, y`* et lance un nouveau MSS. Si aucun objet sélectionnable n’est à l’emplacement de sélection ou si l’emplacement de sélection n’est pas valide, l’action spécifiée par `attribute::OnFailSel` est prise.

*`level`* Indique s’il convient de sélectionner le groupe le plus éloigné ou d’effectuer une analyse approfondie vers un groupe ou un objet imbriqué. If *`level`* n’est pas spécifié, le groupe le plus éloigné est sélectionné. Définissez cette variable sur 1 pour sélectionner un niveau de groupe sous le groupe le plus éloigné. Définissez cette variable sur un nombre élevé (99, par exemple) pour sélectionner l’objet ou le groupe le plus sélectionnable.

## Propriétés {#section-8f27e84d88734a62a5e398e0c9972bdc}

la commande Sélection; Délimiteur MSS. La sélection d’objet est persistante jusqu’à ce qu’un autre objet soit sélectionné, avec la méthode `obj=` ou `sel=`.

*`x, y`* Doit se trouver dans la plage 0, 0 (coin supérieur gauche de l’image) pour *`wid`*-1, *`hei`*-1 (coin inférieur droit de l’image), où *`wid`* et *`hei`* est la taille de la vignette sans mise à l’échelle.

Si spécifié, *`level`* doit être égal ou supérieur à 0.

## Par défaut {#section-e13c705a3e76468894b4ec190ed8a893}

Aucun pour *`x, y`*. *`level`* La valeur par défaut est 0.

## Voir aussi {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
