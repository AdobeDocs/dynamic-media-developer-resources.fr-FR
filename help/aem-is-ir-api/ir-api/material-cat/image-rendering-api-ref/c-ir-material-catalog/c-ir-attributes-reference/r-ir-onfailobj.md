---
description: Gestion des erreurs de sélection d’objet. Spécifie l’action à effectuer si la commande obj= échoue, car le chemin spécifié ne peut pas être mis en correspondance dans la hiérarchie d’objets de vignette.
seo-description: Gestion des erreurs de sélection d’objet. Spécifie l’action à effectuer si la commande obj= échoue, car le chemin spécifié ne peut pas être mis en correspondance dans la hiérarchie d’objets de vignette.
seo-title: OnFailObj
solution: Experience Manager
title: OnFailObj
topic: Scene7 Image Serving - Image Rendering API
uuid: b9dcaf29-ffa5-47db-9c8c-d1809da73582
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# OnFailObj{#onfailobj}

Gestion des erreurs de sélection d’objet. Spécifie l’action à effectuer si la commande obj= échoue, car le chemin spécifié ne peut pas être mis en correspondance dans la hiérarchie d’objets de vignette.

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
  <td class="stentry"> <p>Désélectionner ; toute tentative d’application d’une matière ou d’affichage/masquage d’objets sera ignorée. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Renvoyer une erreur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Sélectionnez le groupe par défaut (le premier groupe de la hiérarchie de vignettes qui contient des objets à rendu). </p> </td> 
 </tr> 
</table>

## Par défaut {#section-a5a95a2b4a204a4eae350e5b544d1513}

Hérité de `default::OnFailObj` si non définie.

## Voir aussi {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
