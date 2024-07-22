---
title: OnFailSel
description: Gestion des erreurs de sélection. Indique l’action à effectuer si la commande sel= échoue, car l’emplacement de pixel spécifié ne se trouve pas dans la zone de masque d’un objet sélectionnable.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d5485569-def8-4e16-9f0e-7dd30d38439d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 6%

---

# OnFailSel{#onfailsel}

Gestion des erreurs de sélection. Spécifie l’action à effectuer si la commande `sel=` échoue, car l’emplacement de pixel spécifié ne se trouve pas dans la zone de masque d’un objet sélectionnable.

## Propriétés {#section-cec491e6c5c744f9bfafaaa9d8774f83}

Enum.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p> </td> 
  <td class="stentry"> <p>Hériter de <span class="codeph"> default::OnFailSel </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Conservez la sélection précédente. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Désélectionnez cette option ; toute tentative d’application d’un matériau ou d’affichage/masquage d’objets est ignorée. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Renvoie une erreur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Sélectionnez le groupe par défaut (le premier groupe de la hiérarchie de vignettes contenant les objets à rendre). </p> </td> 
 </tr> 
</table>

## Par défaut {#section-c25f458f9f8f4236963a95779529e664}

Hérité de `default::OnFailSel` si elle n’est pas définie.

## Voir aussi {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) , [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
