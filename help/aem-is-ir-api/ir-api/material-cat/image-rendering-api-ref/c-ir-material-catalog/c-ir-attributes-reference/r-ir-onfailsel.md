---
description: Gestion des erreurs de sélection. Indique l’action à effectuer en cas d’échec de la commande sel=, car l’emplacement de pixel spécifié ne se trouve pas dans la zone de masque d’un objet sélectionnable.
seo-description: Gestion des erreurs de sélection. Indique l’action à effectuer en cas d’échec de la commande sel=, car l’emplacement de pixel spécifié ne se trouve pas dans la zone de masque d’un objet sélectionnable.
seo-title: OnFailSel
solution: Experience Manager
title: OnFailSel
topic: Scene7 Image Serving - Image Rendering API
uuid: 073b6651-970c-460c-b044-e3ef37cc677a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# OnFailSel{#onfailsel}

Gestion des erreurs de sélection. Indique l’action à effectuer en cas d’échec de la commande sel=, car l’emplacement de pixel spécifié ne se trouve pas dans la zone de masque d’un objet sélectionnable.

## Propriétés {#section-cec491e6c5c744f9bfafaaa9d8774f83}

Enum.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p> </td> 
  <td class="stentry"> <p>Hériter de <span class="codeph"> default::OnFailSel </span>. </p> </td> 
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

## Par défaut {#section-c25f458f9f8f4236963a95779529e664}

Hérité de `default::OnFailSel` si non définie.

## Voir aussi {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) , [attribut::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
