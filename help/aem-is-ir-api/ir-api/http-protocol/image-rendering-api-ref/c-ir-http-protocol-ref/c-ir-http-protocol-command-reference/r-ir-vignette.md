---
title: vignette
description: Fichier vignette. Indique la vignette à utiliser pour la requête.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# vignette{#vignette}

Fichier vignette. Indique la vignette à utiliser pour la requête.

`vignette=[ *`catId`*/] *`recId`*|[catId/] *`file`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>Identifiant du catalogue de matières (correspondant à l’attribut <span class="codeph">::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Identifiant de la vignette (correspond à <span class="codeph"> vignette::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p></td> 
  <td class="stentry"> <p>Chemin et nom relatifs du fichier de vignette. </p></td> 
 </tr> 
</table>

Peut spécifier une entrée de vignette ou un fichier de vignette. Les URL distantes ne sont pas autorisées.

`vignette=` Peut être utilisé comme alternative à la spécification de la vignette dans le chemin de l’URL de requête. Permet de spécifier des vignettes au moyen de variables dans les modèles.

Si *`catId`* n’est pas spécifié, le catalogue de sessions est utilisé.

## Propriétés {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Peut se produire n’importe où dans la requête. Permet de remplacer la vignette spécifiée par le chemin de l’URL de requête.

## Par défaut {#section-db0618d48bc84dc8abcc989550349ccc}

Aucune

## Voir aussi {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Catalogues de matières](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [Variables personnalisées](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
