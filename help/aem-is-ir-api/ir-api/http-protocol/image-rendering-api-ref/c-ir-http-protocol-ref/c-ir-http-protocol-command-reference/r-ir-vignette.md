---
title: vignette
description: Fichier Vignette. Spécifie la vignette à utiliser pour la demande.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
TQID: 'https://experienceleague.adobe.com/tEmCtPpiV1Y61y8R2kji-iBDwWCP3obkDR-K23AaewE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 119
ht-degree: 3%

---

# vignette{#vignette}

Fichier Vignette. Spécifie la vignette à utiliser pour la demande.

`vignette=[ *`catId`*/] *`recId`*|[catId/] *`file`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>ID catalogue de matières (correspondant à <span class="codeph"> attribut::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>ID de vignette (correspondant à <span class="codeph"> vignette::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fichier </span> </p></td> 
  <td class="stentry"> <p>Chemin et nom du fichier de vignette relatif. </p></td> 
 </tr> 
</table>

Vous pouvez spécifier une entrée de carte de vignette ou un fichier de vignette. Les URL distantes ne sont pas autorisées.

`vignette=` Peut être utilisé comme alternative à la spécification de la vignette dans le chemin d’accès de l’URL de requête. Utilisé pour spécifier des vignettes au moyen de variables dans des modèles.

Si *`catId`* n’est pas spécifié, le catalogue de sessions est utilisé.

## Propriétés {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Peut se produire n’importe où dans la requête. Remplace la vignette spécifiée avec le chemin d’accès à l’URL de la requête.

## Par défaut {#section-db0618d48bc84dc8abcc989550349ccc}

Aucune

## Voir aussi {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Catalogues de matières](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [Variables personnalisées](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
