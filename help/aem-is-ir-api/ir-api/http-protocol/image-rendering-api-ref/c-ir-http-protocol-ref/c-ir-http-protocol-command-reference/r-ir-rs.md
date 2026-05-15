---
title: rs
description: Paramètres de rendu avancés. Indique les paramètres de rendu avancés à appliquer lors du rendu de la sélection en cours.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
TQID: 'https://experienceleague.adobe.com/-wOy--XUu7TX6-rwrUFpuqz82bOwb4wpA9Pa0pM8J-4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 3%

---

# rs{#rs}

Paramètres de rendu avancés. Indique les paramètres de rendu avancés à appliquer lors du rendu de la sélection en cours.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Chaîne des paramètres de rendu. </p></td> 
 </tr> 
</table>

Utilisé pour affiner l’aspect du rendu. Pour créer des chaînes de paramètres de rendu, utilisez la fonction de rendu de l’outil de création de vignettes (qui fait partie du package de création d’images Dynamic Media).

## Propriétés {#section-9a2b2228789046658cb80eddf343af75}

Attribut Material.

## Par défaut {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Exemple {#section-47e4811882574441a4d517e42a35f352}

Après quelques essais dans la création d’images, il est déterminé que le masquage flou (USM) fournit la quantité correcte d’accentuation pour l’application et le matériau donnés. La chaîne des paramètres de rendu qui configure USM est copiée dans la commande `rs=` à utiliser avec ce matériau :

`…&rs=U2V20W50X2&…`

## Voir aussi {#section-930116e735024a008c994547ba36ee40}

[catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
