---
title: vignette
description: Fichier de vignette. Spécifie la vignette à utiliser pour la demande.
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

Fichier de vignette. Spécifie la vignette à utiliser pour la demande.

`vignette=[ *`fichier recId catId`*/] *` `*|[catId/] *` `*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ID cat.</span> </p> </td> 
  <td class="stentry"> <p>ID du catalogue des matériaux (correspondant à l’attribut <span class="codeph">  ::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Identifiant de vignette (correspondant à <span class="codeph"> vignette ::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> lime</span> </p></td> 
  <td class="stentry"> <p>Nom et chemin d’accès relatifs au fichier de vignettes. </p></td> 
 </tr> 
</table>

Il peut spécifier une entrée de mappage ou un fichier de vignette. Les URL distantes ne sont pas autorisées.

`vignette=` Peut être utilisé au lieu de spécifier la vignette dans le chemin d’URL de requête. Utilisé pour spécifier des vignettes par le biais de variables dans des modèles.

Si *`catId`* cette option n’est pas spécifiée, le catalogue des sessions est utilisé.

## Propriétés {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Peut se produire n’importe où dans la requête. Remplace la vignette spécifiée par le chemin d’URL de requête.

## Par défaut {#section-db0618d48bc84dc8abcc989550349ccc}

Aucune

## Voir aussi {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[catalogues](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2) de matériaux, [variables personnalisées](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
