---
description: Fichier de vignette. Indique la vignette à utiliser pour cette demande.
solution: Experience Manager
title: vignette
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 4%

---


# vignette{#vignette}

Fichier de vignette. Indique la vignette à utiliser pour cette demande.

`vignette=[ *``*/] *``*|[catId/] *`catIdrecIdfile`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>ID de catalogue de matières (correspond à l'attribut <span class="codeph">::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Identifiant de la vignette (correspond à <span class="codeph"> vignette::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p></td> 
  <td class="stentry"> <p>Chemin et nom relatifs du fichier de vignettes. </p></td> 
 </tr> 
</table>

Peut spécifier une entrée de mappage de vignettes ou un fichier de vignette. Les URL distantes ne sont pas autorisées.

`vignette=` peut être utilisée comme alternative à la spécification de la vignette dans le chemin d’accès de l’URL de requête. Principalement utilisé pour spécifier des vignettes au moyen de variables dans les modèles.

Si *`catId`* n&#39;est pas spécifié, le catalogue de sessions est utilisé.

## Propriétés {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Peut se produire n’importe où dans la demande. Remplace la vignette spécifiée par le chemin d’accès de l’URL de demande.

## Par défaut {#section-db0618d48bc84dc8abcc989550349ccc}

Aucune

## Voir aussi {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Catalogues](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2) de matières, variables  [personnalisées](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
