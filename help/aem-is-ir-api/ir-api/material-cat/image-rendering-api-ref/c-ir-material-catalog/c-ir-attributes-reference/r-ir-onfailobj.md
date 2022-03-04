---
description: Gestion des erreurs de sélection d’objet. Indique l’action à effectuer si la commande obj= échoue, car le chemin spécifié ne peut pas être mis en correspondance dans la hiérarchie d’objets de vignette.
solution: Experience Manager
title: OnFailObj
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0ed04daf-1797-4c12-ae6d-a9a008de9d1d
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 14%

---

# OnFailObj{#onfailobj}

Gestion des erreurs de sélection d’objet. Indique l’action à effectuer si la commande obj= échoue, car le chemin spécifié ne peut pas être mis en correspondance dans la hiérarchie d’objets de vignette.

## Propriétés {#section-2c779d9c133a443d9f0aed9fde7b703c}

Enum.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p> </td> 
  <td class="stentry"> <p>Hériter de <span class="codeph"> default::OnFailObj </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Conserver la sélection précédente. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Désélectionner ; toute tentative d’application d’un matériau ou d’affichage/masquage d’objets est ignorée. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Renvoyer une erreur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Sélectionnez le groupe par défaut (le premier groupe de la hiérarchie de vignettes contenant les objets à rendre). </p> </td> 
 </tr> 
</table>

## Par défaut {#section-a5a95a2b4a204a4eae350e5b544d1513}

Hérité de `default::OnFailObj` si elle n’est pas définie.

## Voir aussi {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
