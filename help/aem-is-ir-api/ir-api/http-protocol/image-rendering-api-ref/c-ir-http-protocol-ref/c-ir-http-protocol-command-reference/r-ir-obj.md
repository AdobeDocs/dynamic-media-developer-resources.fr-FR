---
title: obj
description: Sélectionnez l’objet par nom. Sélectionne le groupe de vignettes spécifié par son nom et lance un nouveau MSS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# obj{#obj}

Sélectionnez l’objet par nom. Sélectionne le groupe de vignettes spécifié par son nom et lance un nouveau MSS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Nom ou chemin/nom du groupe. </p> </td> 
 </tr> 
</table>

Les sous-groupes ou les objets individuels peuvent être sélectionnés à l’aide d’un chemin d’accès de groupe complet (c’est-à-dire en spécifiant le nom du groupe cible ou de l’objet précédé de tous les groupes parents, séparés par des / (barres obliques).

Si aucun groupe/objet portant le nom spécifié n’est trouvé, l’action spécifiée dans `attribute::OnObjFail` est prise.

## Propriétés {#section-9463b36e8ff74c81a70c7c2b58927430}

la commande Sélection; Délimiteur MSS. La sélection d’objet est persistante jusqu’à ce qu’un autre objet soit sélectionné, avec la méthode `obj=` ou `sel=`.

Les noms et les chemins d’accès aux groupes/objets ne sont pas sensibles à la casse.

## Par défaut {#section-0c322850512c4896bb551856a549440e}

Le premier groupe de la vignette contenant des objets de rendu est automatiquement sélectionné à l’ouverture d’une nouvelle vignette.

## Voir aussi {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
