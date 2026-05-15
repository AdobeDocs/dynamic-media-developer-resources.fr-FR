---
title: CallToAction.align
description: Attribut de configuration pour la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e0a92c4a-3757-4811-87b8-68fb367ea94d
TQID: 'https://experienceleague.adobe.com/zMB6vYFDHiSJW1Q3O-L1204O7PkWg-a-txzamKbtZwQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 3%

---

# CallToAction.align{#calltoaction-align}

Attribut de configuration pour la visionneuse de vidéos interactives.

`[CallToAction.|<containerId>_callToAction.]align=left|center|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche|centre|droite</span> </p> </td> 
   <td colname="col2"> <p> Indique l’alignement horizontal interne (ou ancrage) du conteneur de miniatures dans la zone du composant. </p> <p>Dans call-to-action, le conteneur des miniatures internes est dimensionné de sorte que seul un nombre entier de miniatures soit affiché. Par conséquent, il existe une certaine marge intérieure entre le conteneur interne et les limites du composant externe. </p> <p>Ce modificateur spécifie la manière dont le conteneur de miniatures internes est positionné horizontalement à l’intérieur du composant. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`center`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
align=left
```
