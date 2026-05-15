---
title: setContainerId
description: Référence de l’API JavaScript pour la visionneuse panoramique.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: b0145fb0-2b0d-40ce-ac18-029f54bc4050
autotag-review: '2026-05-13T22:10:33.187Z'
TQID: 'https://experienceleague.adobe.com/4Ndg-s-4Re6hMADDbkBDvKWdGFH8bzHGGooU-rNCraU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 88
ht-degree: 3%

---

# setContainerId{#setcontainerid}

Référence de l’API JavaScript pour la visionneuse panoramique.

` setContainerId( *`containerId`*)`

Définit l’identifiant du conteneur DOM (normalement un DIV) dans lequel la visionneuse est insérée. Il n’est pas nécessaire que l’élément de conteneur soit créé au moment où cette méthode est appelée. Cependant, le conteneur doit exister lors de l’exécution de `init()`. Il doit être appelé avant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec l’objet JSON `config` au constructeur .

## Paramètre {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} ID </span> conteneur. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
