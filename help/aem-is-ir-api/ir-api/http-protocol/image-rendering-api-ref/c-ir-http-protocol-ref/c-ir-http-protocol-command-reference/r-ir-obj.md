---
title: obj
description: Sélectionnez l’objet par nom. Sélectionne le groupe de vignettes spécifié par son nom et lance un nouveau MSS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
TQID: 'https://experienceleague.adobe.com/te9iyNajxDfgvHqqThbVUc7tBItxfMtxhOMl2eCLOsk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 3%

---

# obj{#obj}

Sélectionnez l’objet par nom. Sélectionne le groupe de vignettes spécifié par son nom et lance un nouveau MSS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Nom du groupe ou chemin/nom. </p> </td> 
 </tr> 
</table>

Les sous-groupes ou les objets individuels peuvent être sélectionnés à l’aide d’un chemin de groupe complet (c’est-à-dire en spécifiant le nom du groupe cible ou de l’objet précédé de tous les groupes parents, séparé par / (barres obliques).

Si aucun groupe/objet portant le nom spécifié n’est trouvé, l’action spécifiée dans `attribute::OnObjFail` est exécutée.

## Propriétés {#section-9463b36e8ff74c81a70c7c2b58927430}

Commande de sélection ; délimiteur MSS. La sélection d&#39;objet est persistante jusqu&#39;à ce qu&#39;un autre objet soit sélectionné, avec `obj=` ou `sel=`.

Les chemins et noms de groupe/objet ne respectent pas la casse.

## Par défaut {#section-0c322850512c4896bb551856a549440e}

Le premier groupe de la vignette contenant les objets rendus est sélectionné automatiquement lorsqu’une nouvelle vignette est ouverte.

## Voir aussi {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)

