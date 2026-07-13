---
title: sous-marin
description: Sous-sélection. Permet d'appliquer différents matériaux à différentes zones de l'objet ou du groupe sélectionné et de supprimer les matériaux précédemment appliqués.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9968fbb-c38b-4180-81be-19992fa8f347
TQID: 'https://experienceleague.adobe.com/1vZwrwUBziB5UYudKf6n-eKQP2Weluqjo1iiVDMSUms'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 6%

---

# sous-marin{#sub}

Sous-sélection. Permet d&#39;appliquer différents matériaux à différentes zones de l&#39;objet ou du groupe sélectionné et de supprimer les matériaux précédemment appliqués.

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
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
  <td class="stentry"> <p>Sélectionnez la zone de bordure du mur supérieur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Sélectionnez la zone de la bordure du mur central. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Sélectionnez la zone de bordure du mur inférieur. </p> </td> 
 </tr> 
</table>

Actuellement pris en charge uniquement pour les objets de mur. Termine un MSS précédent et en démarre un nouveau pour la matière à appliquer à la sous-sélection spécifiée.

Un matériau spécifié pour le mur supérieur ou inférieur s&#39;applique à l&#39;ensemble du mur, sauf si un autre matériau a également été spécifié pour l&#39;autre moitié du mur.

## Propriétés {#section-b202139d6d0847cc8d520a154104ab9d}

Commande de sélection ; délimiteur MSS.

## Par défaut {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Voir aussi {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)

