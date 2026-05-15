---
title: sel
description: Sélectionnez l’objet en fonction de l’emplacement en pixels.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
TQID: 'https://experienceleague.adobe.com/nmXZZFxdpxJTY4j12JRyhCe-sOZIjajFSfzmPId9X3g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 1%

---

# sel{#sel}

Sélectionnez l’objet en fonction de l’emplacement en pixels.

` sel= *`x`*, *`y`*[, *`level`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>Choisissez les coordonnées de localisation en pixels (int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> de niveau <span class="varname"> </p> </td> 
  <td class="stentry"> <p>Niveau du groupe (int). </p> </td> 
 </tr> 
</table>

Sélectionne le groupe ou l&#39;objet aux coordonnées en pixels spécifiées par *`x, y`* et lance un nouveau MSS. Si aucun objet sélectionnable ne se trouve à l&#39;emplacement de prélèvement ou si cet emplacement n&#39;est pas valide, l&#39;action spécifiée par `attribute::OnFailSel` est exécutée.

*`level`* Indique s’il faut sélectionner le groupe le plus à l’extérieur ou accéder à un groupe ou un objet imbriqué. Si *`level`* n’est pas spécifié, le groupe le plus à l’extérieur est sélectionné. Définissez sur 1 pour sélectionner un niveau de groupe sous le groupe le plus à l’extérieur. Définissez sur un grand nombre (99, par exemple) pour sélectionner l’objet ou le groupe sélectionnable le plus à l’intérieur.

## Propriétés {#section-8f27e84d88734a62a5e398e0c9972bdc}

Commande de sélection ; délimiteur MSS. La sélection d&#39;objet est persistante jusqu&#39;à ce qu&#39;un autre objet soit sélectionné, avec `obj=` ou `sel=`.

*`x, y`* Doit être compris entre 0, 0 (coin supérieur gauche de l’image) et *`wid`*-1, *`hei`*-1 (coin inférieur droit de l’image), où *`wid`* et *`hei`* correspond à la taille de la vue de la vignette non mise à l’échelle.

Si spécifié, *`level`* doit être supérieur ou égal à 0.

## Par défaut {#section-e13c705a3e76468894b4ec190ed8a893}

Aucun pour *`x, y`*. *`level`* La valeur par défaut est 0.

## Voir aussi {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
