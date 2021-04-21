---
description: Sous-sélection. Permet d'appliquer des matériaux différents à différentes zones de l'objet ou du groupe sélectionné, ainsi que de supprimer des matériaux précédemment appliqués.
solution: Experience Manager
title: sub
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 6%

---


# sub{#sub}

Sous-sélection. Permet d&#39;appliquer des matériaux différents à différentes zones de l&#39;objet ou du groupe sélectionné, ainsi que de supprimer des matériaux précédemment appliqués.

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p> </td> 
  <td class="stentry"> <p>Sélectionnez le mur entier. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Sélectionnez la moitié supérieure du mur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Sélectionnez la moitié inférieure du mur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Sélectionnez la zone de bordure supérieure du mur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Sélectionnez la zone de bordure du mur central. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Sélectionnez la zone de bordure inférieure du mur. </p> </td> 
 </tr> 
</table>

Actuellement uniquement pris en charge pour les objets wall. Cesse un MSS précédent et début un nouveau MSS pour le matériau à appliquer à la sous-sélection spécifiée.

Un matériau spécifié pour la paroi supérieure ou inférieure s&#39;applique à l&#39;ensemble de la paroi à moins qu&#39;un autre matériau pour l&#39;autre moitié de la paroi n&#39;ait été spécifié également.

## Propriétés {#section-b202139d6d0847cc8d520a154104ab9d}

Sélection, commande; Délimiteur MSS.

## Par défaut {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Voir aussi {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
