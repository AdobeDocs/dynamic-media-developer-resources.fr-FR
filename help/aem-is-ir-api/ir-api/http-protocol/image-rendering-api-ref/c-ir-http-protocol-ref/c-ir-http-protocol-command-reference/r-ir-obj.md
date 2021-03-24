---
description: Sélectionnez un objet par nom. Sélectionne le groupe de vignettes spécifié par son nom et début un nouveau MSS.
solution: Experience Manager
title: obj
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# obj{#obj}

Sélectionnez un objet par nom. Sélectionne le groupe de vignettes spécifié par son nom et début un nouveau MSS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nom ou chemin/nom du groupe. </p> </td> 
 </tr> 
</table>

Il est possible de sélectionner des sous-groupes ou des objets individuels à l&#39;aide d&#39;un chemin de groupe complet (c&#39;est-à-dire en spécifiant le nom de la Population cible ou de l&#39;objet précédé de tous les groupes parents, séparé par / (barres obliques).

Si aucun groupe/objet portant le nom spécifié n&#39;est trouvé, l&#39;action spécifiée dans `attribute::OnObjFail` est exécutée.

## Propriétés {#section-9463b36e8ff74c81a70c7c2b58927430}

Sélection, commande; Délimiteur MSS. La sélection d’objet est persistante jusqu’à ce qu’un autre objet soit sélectionné, soit avec `obj=` ou `sel=`.

Les chemins d’accès aux groupes/objets et les noms ne sont pas sensibles à la casse.

## Par défaut {#section-0c322850512c4896bb551856a549440e}

Le premier groupe de la vignette contenant des objets à rendu est automatiquement sélectionné à l’ouverture d’une nouvelle vignette.

## Voir aussi {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b),  [attribut::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
