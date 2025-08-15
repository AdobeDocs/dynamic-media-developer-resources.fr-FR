---
title: Commandes de sélection
description: Ces commandes sont utilisées pour sélectionner des groupes de vignettes, des objets, des sous-zones de groupes ou des objets.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43f6ec6e-e4eb-468d-9c66-841af5e0a8a5
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# Commandes de sélection{#selection-commands}

Ces commandes sont utilisées pour sélectionner des groupes de vignettes, des objets, des sous-zones de groupes ou des objets.

La commande, ou le matériau, ou les deux, sont spécifiés après cette commande de sélection et avant que la commande de sélection suivante (ou la fin de la requête) ne soit appliquée à l’élément sélectionné. Les commandes de sélection délimitent des segments MSS (Material Specification).

<table id="simpletable_028957E516644FE8A7B1BC056A32FCD1"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a" type="reference" format="dita" scope="local"> Obj</a> </span> </p></td> 
  <td class="stentry"> <p>Sélectionnez un groupe de vignettes ou un objet par nom. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b" type="reference" format="dita" scope="local"> sel</a></span> </p></td> 
  <td class="stentry"> <p>Sélectionnez un groupe de vignettes ou un objet par emplacement de pixel. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-decal.md#reference-3a5f1adc7fe24c91aa5655d64038e857" type="reference" format="dita" scope="local"> décalque</a></span> </p></td> 
  <td class="stentry"> <p>Sélectionnez la zone de décalcomanie de l’objet sélectionné. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sub.md#reference-3cedba817f3c401495ba32bd1bf9b383" type="reference" format="dita" scope="local"> sub</a></span> </p></td> 
  <td class="stentry"> <p>Sélectionnez une sous-zone du groupe ou de l’objet sélectionné. </p></td> 
 </tr> 
</table>
