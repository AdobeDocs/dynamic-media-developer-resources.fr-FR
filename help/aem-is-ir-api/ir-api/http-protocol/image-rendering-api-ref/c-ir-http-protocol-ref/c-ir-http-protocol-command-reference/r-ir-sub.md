---
title: sub
description: Sous-sélection. Permet d’appliquer différents matériaux à différentes zones de l’objet ou du groupe sélectionné et de supprimer les matériaux précédemment appliqués.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9968fbb-c38b-4180-81be-19992fa8f347
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 6%

---

# sub{#sub}

Sous-sélection. Permet d’appliquer différents matériaux à différentes zones de l’objet ou du groupe sélectionné et de supprimer les matériaux précédemment appliqués.

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p> </td> 
  <td class="stentry"> <p>Sélectionnez l’intégralité du mur. </p> </td> 
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
  <td class="stentry"> <p>Sélectionnez la zone de bordure du mur du milieu. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Sélectionnez la zone de bordure du mur inférieur. </p> </td> 
 </tr> 
</table>

Actuellement prise en charge uniquement pour les objets muraux. Met fin à un MSS précédent et démarre un nouveau MSS pour le matériau à appliquer à la sous-sélection spécifiée.

Un matériau spécifié pour la paroi supérieure ou inférieure s’applique à l’ensemble du mur, à moins qu’un matériau différent pour l’autre moitié du mur n’ait également été spécifié.

## Propriétés {#section-b202139d6d0847cc8d520a154104ab9d}

Commande de sélection ; Délimiteur MSS.

## Par défaut {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Voir aussi {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
