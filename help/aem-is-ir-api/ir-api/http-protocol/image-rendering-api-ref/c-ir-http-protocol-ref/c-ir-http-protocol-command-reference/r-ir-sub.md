---
description: Sous-sélection. Permet d’appliquer différents matériaux à différentes zones de l’objet ou du groupe sélectionné, ainsi que de supprimer les matériaux précédemment appliqués.
solution: Experience Manager
title: sub
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: c9968fbb-c38b-4180-81be-19992fa8f347
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 6%

---

# sub{#sub}

Sous-sélection. Permet d’appliquer différents matériaux à différentes zones de l’objet ou du groupe sélectionné, ainsi que de supprimer les matériaux précédemment appliqués.

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
  <td class="stentry"> <p>Sélectionnez la zone de bordure du mur inférieur. </p> </td> 
 </tr> 
</table>

Actuellement pris en charge uniquement pour les objets wall. Termine un MSS précédent et lance un nouveau MSS pour le matériau à appliquer à la sous-sélection spécifiée.

Un matériau spécifique pour la paroi supérieure ou inférieure s&#39;appliquera à l&#39;ensemble du mur à moins qu&#39;un autre matériau pour l&#39;autre moitié du mur n&#39;ait été spécifié également.

## Propriétés {#section-b202139d6d0847cc8d520a154104ab9d}

la commande Sélection; Délimiteur MSS.

## Par défaut {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Voir aussi {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
